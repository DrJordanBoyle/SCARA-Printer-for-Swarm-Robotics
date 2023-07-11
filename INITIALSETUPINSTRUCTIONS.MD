# INITIAL INSTRUCTIONS BEFORE PRINTING
The current version of the printer utilizing any limit switches yet, therefore before printing it is necessary to 'home' the system properly by hand. In general the method involves placing the arm at a dinstinct position and using G-CODE to tell the system where its positioned at. From there, the system can function normally.

### Important to note
- The current bed size is set at x-dimension = 60 mm and y-dimension = 200 mm.
- The end effector can move outside of the set bed space, but there is risk of reaching coordinates that are unattainable which will cause malfunctions.
- This project used 'Pronterface' to connect and interact with the printer using a computer, there are other softwares that do the same.

### Step by step instructions
1. Connect the motherboard with a computer with Pronterface using the given USB cable (micro USB probably).

2. Make sure you are using the correct port by selecting the port on the top left, and also make sure the baudrate is set to the correct value which can be found next to the port settings. In this case, using the BTT SKR Mini E3 the baudrate should be set to 115200.

![Pronterface interface](https://github.com/MigraineMonster/SCARA-Printer-for-Swarm-Robotics/assets/129239045/872d8f81-bb58-4bb5-955e-9baecc32c4dd)

3. On the top left, you can press connect and a message should pop up in the serial monitor on the right side that says "Printer is now online.".

4. Place the arms/links straight out in front of the machine, making sure that the angles theta1 and theta2 are 90 degrees (or as near as possible).

![How to initially setup the links](https://github.com/MigraineMonster/SCARA-Printer-for-Swarm-Robotics/assets/129239045/ae2f248a-3458-46ab-94c9-de808198a1d1)

5. Using an interface such as Pronterface, use G-CODE G92 to indicate the current position. Fill out "G92 X50 Y109.5". This position was calculated as the coordinates of the end effector when theta1 and theta2 are 90 degrees. 


6. From here, you should be able to use G-CODE G1 to move around the end effector. The center of this print area can be found at (30,100). Use "G1 X30 Y100" to move the end effector to the middle of the 'bed'.

7. Now the Z-axis position must be homed, using the interface on pronterface keep moving the z-axis down until the hot-end is near the surface. Use a piece of A4 paper and place it between the hot end and the surface, you want to be able to move the paper around freely with some minor resistance. When that point is found, use "G92 Z0" to indicate the positioning of the Z-Axis.

8. IMPORTANT: Turn on the fan manually and set to 100% before printing! Use "M106 P2 S255" to set the hot end fan to 100%.

