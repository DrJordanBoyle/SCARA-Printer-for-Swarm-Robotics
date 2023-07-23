# Marlin Code Log

In this segment information is given in regards to what alterations were done to the original Marlin code to have the machine up and running. Good to note is that some changes may have been undocumented. I have tried to add comments to every adjustment, but only wrote them down at the end. It was a long process, you may find an altered line of code that is not documented in this file! You can contact me to update the document. General information on how to work and compile Marlin firmware can be found online. The motherboard we used was generally used to upgrade Creality machines, so some specific adjustments needed to be made. But again, this information can be found online :)

- Marlin version 2.0.9.5
- BTT SKR Mini E3 V3.0 motherboard
- E3D V6 Hot end

## Files that have been altered

- Configuration.h
- scara.cpp

## Configuration.h

- #define MOTHERBOARD BOARD_BTT_SKR_MINI_E3_V3_0 // Line ~90, adjust to own motherboard
- Line ~101 // adjust SERIAL_PORT to your motherboard’s settings
- Line ~114 // adjust BAUDRATE to your motherboard’s baudrate settings
- Line ~154-155 // SCARA_CROSSTALK_FACTOR and SCARA_IS_RIGHT_HANDED variables added to be able to work with different mechanisms. This system does not use an intermediate pulley and is right handed. Its full function can be found in scara.cpp.

#define SCARA_CROSSTALK_FACTOR 1

#define SCARA_IS_RIGHT_HANDED 1

- Line ~157 // define MP_SCARA to be able to use SCARA specific commands and functions
- Line 210-221 // Adjust driver type to the ones your system uses, our motherboard has integrated TMC 2209 drivers.
- Line 562 // Adjust temp_SENSOR_0 to the correct thermistor (we have E3D)
- Line 1098 // Adjust the DEFAULT_AXIS_STEPS_PER_UNIT depending on each stepper’s resolution and micro stepping settings.
- Line 1147-1164 // Some jerk settings were adjusted based on SCARA systems found online
- Line 1590-1601 // Bed dimensions and end stop positions were adjusted. Currently the safe working space is at X = 200 mm and Y = 60 mm. The current home position is set to the corner, but is not used at all in the current operation.

## Scara.cpp

- Line 35 // SCARA_CROSSTALK_FACTOR function added that changes it to 0 if not defined
- Line 56-65 // Forward kinematics were adjusted to include the crosstalk factor, some other older forward kinematics can be found in the file.

```
void forward_kinematics(const_float_t a, const_float_t b) {
  
    const float a_sin = sin(RADIANS(a)) * L1,
                a_cos = cos(RADIANS(a)) * L1,
                b_sin = sin(RADIANS(b + a * SCARA_CROSSTALK_FACTOR)) * L2,
                b_cos = cos(RADIANS(b + a * SCARA_CROSSTALK_FACTOR)) * L2;

    cartes.x = a_cos + b_cos + scara_offset.x;  // theta
    cartes.y = a_sin + b_sin + scara_offset.y;  // phi
```

- Line 172-193 // Some things were adjusted to fine tune the homing settings, but was never tested.
- Line 197 - 218 // Inverse kinematics were added with the SCARA_IS_RIGHT_HANDED and SCARA_CROSSTALK_FACTOR variables integrated into them. More explanation can be found in the code comments. Another line of code was added to see the exact position on the serial monitor.

```cpp
const float x = raw.x - scara_offset.x, y = raw.y - scara_offset.y,             // Finding the desired position, relative to the shoulder location
                hand = SCARA_IS_RIGHT_HANDED ? 1 : -1,                              // Make the SCARA RHS or LHS
                THETA3 = ATAN2(y, x), c2 = HYPOT2(x, y), rc = RSQRT(c2),            // THETA3 is found by simply using inverse tangens with the x and y coordinates of ee           
                THETA1 = THETA3 - hand * ACOS((c2 + sq(L1) - sq(L2)) * rc * RECIPROCAL(2.0f * L1)),   // THETA1 can be found by deducting angle ALFA from THETA3
                THETA2 = THETA3 + hand * ACOS((c2 + sq(L2) - sq(L1)) * rc * RECIPROCAL(2.0f * L2));   // THETA2 is found by deducting

    

    delta.set(DEGREES(THETA1), DEGREES(THETA2 - THETA1 * SCARA_CROSSTALK_FACTOR), raw.z);   // Sets the THETA1 and THETA2 values in degrees, the SCARA_CROSSTALK_FACTOR is added for non-intermediate pulley systems.

    SERIAL_ECHOLNPGM("  SCARA (x,y) ", x, "   ,  ", y," Theta1=", DEGREES(THETA1), " Theta2=", DEGREES(THETA2));
```

- Line 360-370 // Some more code was added for the serial monitor during setup.
