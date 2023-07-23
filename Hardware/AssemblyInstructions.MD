# Assembly instructions SCARA ARM

## General components overview

![image](https://github.com/MigraineMonster/SCARA-Printer-for-Swarm-Robotics/assets/129239045/9aa6aaab-4435-4f46-8872-ab3884676ad9)
![image](https://github.com/MigraineMonster/SCARA-Printer-for-Swarm-Robotics/assets/129239045/4e0d0d4e-0736-4bac-bb16-67041daf19b5)
![image](https://github.com/MigraineMonster/SCARA-Printer-for-Swarm-Robotics/assets/129239045/5f7298cf-0f1d-4c22-ae8c-78f2426083e6)
![image](https://github.com/MigraineMonster/SCARA-Printer-for-Swarm-Robotics/assets/129239045/a2cfe844-31cd-4113-bfd4-edc5b63c4e82)

## Part 1: Assemble the Tower

Consists of the base, top plate, x2 shoulder plates (top and bottom).

### Preparing the base, top plate and shoulder plates

- Begin by placing the base on a flat surface and securely attach the rod clamps using M3 bolts and nuts. The base is designed with compartments on the bottom to accommodate the nuts conveniently.
    
![SCARAPRINTER_VERS A v25](https://github.com/MigraineMonster/SCARA-Printer-for-Swarm-Robotics/assets/129239045/33a1fb6e-7860-4f78-9d27-ca9864dbd26d)
    
- Next, carefully insert the three smooth rods into the attached rod clamps on the bottom base. Use another set of M3 bolts and nuts to secure the rods in place. Ensure the rods are aligned properly for smooth movement and stability.
    
![SCARAPRINTER_VERS A v251](https://github.com/MigraineMonster/SCARA-Printer-for-Swarm-Robotics/assets/129239045/040c4380-2901-4f6e-a117-88ed8285e183)
    
- To begin assembling the top plate/lid, mount the rod clamps onto the plate using M3x16mm bolts, similar to the process used for the base. Place the rod clamps on the face of the plate that is facing towards the base/ground. Make sure to fasten the bolts securely to ensure stability and proper alignment.
- Next, attach the Z-stepper onto the top plate, positioning the shaft towards the ground, just like the rod clamps. Securely fasten the stepper using four M3x16mm nuts and bolts. Double-check the alignment and tighten the nuts and bolts to ensure a stable and reliable connection. This step is crucial for the proper functioning of the printer's vertical movement.
- Attach the Z-coupler to the Z-stepper shaft using the provided bolts. Then, connect the leadscrew to the coupler to complete the assembly of the top plate. Handle it with care, as it plays a crucial role in the printer's precise vertical movement.
    
![SCARAPRINTER_VERS A v25234](https://github.com/MigraineMonster/SCARA-Printer-for-Swarm-Robotics/assets/129239045/5e521cc0-7241-4324-86b5-1c01203e2056)
    
- Begin with the bottom shoulder plate. Insert the three linear bearings (8x15x24) into the designated compartments, ensuring they protrude slightly when fully inserted. Use a rubber hammer for secure fitting; note that this is a permanent installation. Next, attach the lead screw coupler to the plate using M3 bolts and nuts. Ensure the protrusion faces downward for proper functionality.

![SCARAPRINTER_VERS A v253](https://github.com/MigraineMonster/SCARA-Printer-for-Swarm-Robotics/assets/129239045/cbc832c7-7f70-4778-b0a0-540e6e969698)

- Similar to the bottom shoulder plate, prepare the top shoulder plate by inserting the three linear bearings and attaching the lead screw coupler using M3 bolts and nuts. Ensure that the components are securely in place.Partially fasten the stepper motor on the top plate using 2 x M3 nuts and bolts. Use the inner two holes for this step, leaving the two holes near the edge of the plate free for later adjustments and additional components.

![SCARAPRINTER_VERS A v254](https://github.com/MigraineMonster/SCARA-Printer-for-Swarm-Robotics/assets/129239045/1a0350fb-7821-4102-850f-74267acff434)

### Assembling Tower

- Carefully slide the bottom shoulder plate onto the three rods, ensuring that the open-faced bearings are pointing towards the sky. Take your time to align the rods properly before sliding on the bottom shoulder plate. This precaution is essential to avoid any damage to the inner walls of the linear bearings.
- The rest of the assembly can only be done after preparing the arm.

![SCARAPRINTER_VERS A v255](https://github.com/MigraineMonster/SCARA-Printer-for-Swarm-Robotics/assets/129239045/080fb28b-0c1f-4d08-8a0c-0c8d09384e6d)
## Part 2: Assemble the arm

Consists of the elbow link and shoulder link.

### Preparing the shoulder link

- Prepare the shoulder link (plates) by inserting the bearings. On the end that connects to the shoulder plates, there are two compartments on the top and bottom faces of the shoulder plates. Insert two 8x16mm thrust bearings into these compartments. Ensure that the bearings are form-fitted into the compartments securely.

![SCARAPRINTER_VERS A v256](https://github.com/MigraineMonster/SCARA-Printer-for-Swarm-Robotics/assets/129239045/a50f31e8-91f8-4889-8d11-862ff2409458)

- On the other end, there are two compartments again, but this time they can be found on the inside faces of the two plates. Here, you can fit the two angular bearings. The sizes of the angular bearings and thrust bearings are quite different, so there is no way of placing them incorrectly. Ensure that these bearings are inserted all the way in, especially the angular ones, to ensure a secure fit.

![SCARAPRINTER_VERS A v257](https://github.com/MigraineMonster/SCARA-Printer-for-Swarm-Robotics/assets/129239045/6c565291-668f-4d08-a90c-aae14bcae32e)

- Prepare the shoulder arm/link by placing the custom pulleys between the top and bottom shoulder arm plates. Ensure that the pulleys are "sandwiched" by the two shoulder link plates. Position the pulley with no holes on its sides towards the base (where the thrust bearings are located), while the pulley with horizontal holes should be placed towards the end effector (where the angular bearings are). Please note that the latter pulley will only be positioned there for now and not secured yet.
    
![SCARAPRINTER_VERS A v258](https://github.com/MigraineMonster/SCARA-Printer-for-Swarm-Robotics/assets/129239045/9a30b5b8-942f-4658-b0dd-a6bf4a0ae480)
    
- Before securing the pulley near the base, make sure to place the GT2 belt (the longer one) around the pulley while it is positioned between the two shoulder link plates. It's essential to do this before locking the pulley in place, as there won't be a way to place the GT2 belt there afterward. Take care to position the belt properly during this step.
- To secure the pulley near the base, use x6 M3x20 bolts and nuts. Drive them through the two shoulder link plates and the pulley itself, fastening everything together tightly. This will ensure the pulley is securely attached between the plates.
- Position the second stepper motor in the middle of the shoulder link, aligning it with the four holes on each plate. Note that four of these holes have a chamfered side, which should face the ground. The stepper motor's shaft should pass through the hole, pointing towards the bottom plate. Use x4 M3x30 nuts and bolts to secure the stepper motor in place, pushing the bolts through both sets of holes to strengthen the double plate setup. With the stepper motor and custom pulley installed, your shoulder link will become significantly sturdier.
    
![SCARAPRINTER_VERS A v2599](https://github.com/MigraineMonster/SCARA-Printer-for-Swarm-Robotics/assets/129239045/09d0beb2-096c-43cd-b092-2df850ceaa9d)
    

### Assembling the Tower / Arm

- Slide the fully assembled shoulder link onto the smooth rod located in the middle. The thrust bearing in the shoulder link should rest on top of the linear bearing that is secured on the bottom shoulder plate. This arrangement will allow for smooth movement and stability in the shoulder assembly.
- Slide the fully assembled top shoulder plate onto the three smooth rods, taking care to avoid scratching the inside of the linear bearings. Ensure that the protrusion from the compartments for the linear bearings points upward for proper functioning and smooth motion of the shoulder assembly.
- You now have a sandwich with the shoulder link in between the two shoulder plates.

![SCARAPRINTER_VERS A v25894](https://github.com/MigraineMonster/SCARA-Printer-for-Swarm-Robotics/assets/129239045/2b99ad63-8cfa-442e-b6b9-e94b91c7ea55)

- Secure the installed components using the lead screw attached to the lid plate. Insert the lead screw through the couplers on the top and bottom shoulder plates and slowly turn it until the lid reaches the top of the smooth rods. Fasten the smooth rods into the rod clamps on the top/lid to fix the distance between the top and bottom shoulder plates. This ensures stability and proper alignment of the shoulder assembly.
- With the fixed distance, complete the installation of the shoulder stepper by using 2 M3x30 bolts and nuts through both the bottom and top shoulder plates. This double-layer setup adds reinforcement to the assembly, ensuring the shoulder stepper is securely in place.

![SCARAPRINTER_VERS A v25546](https://github.com/MigraineMonster/SCARA-Printer-for-Swarm-Robotics/assets/129239045/667d04d5-a353-4570-8813-91e95ce3c560)

### Preparing the Elbow link and final arm assembly

- You can now start preparing the final link, the elbow link which consists of the link itself, the hot end mount and the hot end.
- Attach the elbow link to the hot end mount with two M3x16 bolts, after which you can place the little coupler piece that reinforces the connection between the link and mount. This little coupler uses two M3x10 bolts.
- Attach the partly assembled elbow link to the shoulder link. The elbow link features a cylindrical protrusion that fits into the holes at the end of the shoulder link. Before inserting the protrusion, ensure that the second custom pulley is placed between the two shoulder link plates, along with the second GT2 belt (the shorter one) positioned on the pulley.
- Once the pulley and belt are in place, insert the protrusion through the three layers. Secure the assembly by using 8 headless bolts, screwing them horizontally into the custom pulley to lock the protrusion in place. While the height to lock in the elbow link is flexible, it is recommended not to position it too far below the shoulder link to minimize stress points in the protrusion.

![SCARAPRINTER_VERS A v25874221](https://github.com/MigraineMonster/SCARA-Printer-for-Swarm-Robotics/assets/129239045/68605c11-a437-46f6-8f24-05653eeb8502)

- Lastly, attach the hot end to its mount using 2x M3x16 nuts and bolts. Insert the nuts into their respective compartments from the side to create a self-locking system. By screwing in the bolts, the hot end will tighten itself securely in place.

![SCARAPRINTER_VERS A v255645](https://github.com/MigraineMonster/SCARA-Printer-for-Swarm-Robotics/assets/129239045/b1fccc90-1506-4c74-ac2a-18132d2d248d)

## Part 3: Final touches

- The extruder stepper can be inserted into the mount and then attached to base plate on the back end by using some nuts and bolts.
- Now the idler pulleys can be installed, there are a total of 2 idler pulley rods which are placed on the elbow link and the shoulder plates. To setup the idler pulleys, you use threaded ends in which the idler pulley is placed in the middle of the threaded ends. It is fixed by using two nuts with a spring ring placed between the nut and idler pulley, tighten to fix the pulley. Both the idler rods are then fixed into the slots by using a ring, spring ring and nuts to tighten it in place, make sure the belt is tensioned enough by sliding the rod in the slot.

![SCARAPRINTER_VERS A v258948945](https://github.com/MigraineMonster/SCARA-Printer-for-Swarm-Robotics/assets/129239045/b14d72e5-a114-4399-81c4-4ff006d5cfaf)

- There are small mounts designed to house the limit switches, you can attach one on the lead screw coupler, the second has no attachment point yet. These limit switches are not integrated into the firmware yet as of time of writing.
- A spool holder, limit switches and filament line holder are not added yet but are advisable to design.

## NOTE
- For the hot end assembly please follow the guide of E3D that you can find online. The temperature settings must be adjusted first to correctly install the hot end.
