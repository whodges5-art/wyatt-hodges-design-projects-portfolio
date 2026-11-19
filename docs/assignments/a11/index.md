# A11 – Motor Selection

## Objective
The objective of this assignment is to select an appropriate motor for the tensile tester designed in A10 and design a way to mount the motor, so the tester works correctly.

## Analyze (Wyatt and Aiden)

**Motor** (Wyatt)

The first part of the assignment is to select a motor that can support the driving torque and rotational speed found during A10. Once I converted the units to oz-in and RPs, I could look at the graph and find an appropriate motor. The motor would need a torque of 37.22 oz-in and a rotational speed ranging from .236 to 11.81 rps. The images below display the math for this.

![Motor Math](Motor.jpeg)
![Motor Graph](MotorGraph.png)

After finding a datasheet detailing different SureStep High Voltage motors, I looked for a graph that would fit these specifications. I tried to find one with a torque speed curve that intersected 37.22 oz-in and 11.81 rps. I found the STP-MTRAC-23044 met my requirements for driving torque and max speed. I then looked to make sure the torque produced at the minimum rps would be below the max allowable torque, 16313 oz-in, which it was.

**Motor Mount** (Wyatt-Math, Aiden-CAD)

For the CAD, the thickness was 0.25in, and we made a cutout for the 1.50in circle on the motor and made the depth the thickness it is on the motor. The rest of the dimensions and math are seen in the images below.

![Mount Math](Mount.jpeg)
![MotorMount1](MotorMount1.png)
![MotorMount2](MotorMount2.png)

**Coupler** (Wyatt-Math, Aiden-CAD)

For the coupler, I needed to determine the necessary outer diameter to support the load in the motor and screw. I used an equation relating shear stress, torque and the bearings cross-sectional area to find the outer diameter. Max stress was set equal to 250 MPa divided by my safety factor of 4 because that is a standard value for steel. The same torque as before was used, and the inner diameter equals the lead screw diameter of 7/8 inches. After looking for an outer diameter, I found it needed to have a total diameter of 2.06 inches. Then, they were inserted into the assembly. These are all shown in the images below.

![Coupler Math](Coupler.jpeg)
![Couplers](Couplers.png)

**Bracket** (Wyatt)

For the bracket, I drew a sketch modeling the twisting caused by the motor torque and the reaction forces involved in the corner brackets that are supposed to keep the cross-beam in place. I found that all the reaction forces would be focused on the screws holding the corner bracket to the extrusion so if the screws could support the load, the bracket would not twist or fall.

![bracket](bracket.jpeg)

## CAD (Aiden)
**Top Frame FEA** (Aiden)

To prepare the FEA for the top frame, everything else was isolated from the assembly except the top frame and motor mounts. Fixed geometry was applied at both ends to simulate being attached to the vertical beams. 6061-T6 was chosen to be the aluminum of the extrusions. Finally, a 1kN load and the calculated 0.2628 N*m were applied to both screw holes. After the first run, I refined the mesh and calculated convergence. In the images below, there are initial FEA results which display the max von Mises, vertical deflection at the grip line and factor of safety. As well as, the calculated convergence from all three.

![feaframegeo](feaframegeo.png)
![feaframeforce](feaframeforce.png)
![feaframe1](feaframe1.png)
![feaframe2](feaframe2.png)
![feaframe3](feaframe3.png)
![feaframe5](feaframe5.png)

The stress is way larger than expected, in the image below is the point where the stress is concentrated the most. In order to make this smaller, we could've used a larger aluminum extrusion to make the stress concentration less.

![feaframe4](feaframe4.png)

**Vertical FEA** (Aiden)

To prepare the FEA for the vertical frame, I removed all the set screw components. I added fixed geometries to the bottom extrusions and then applied my forces on the top. 6061-T6 was used as the material for all the components and a 1 kN load was applied to the top of the motor mounts. In the images below are the results, which display the max von Mises, vertical deflection at the grip line and factor of safety.

![feaverticalforce](feaverticalforce.png)
![feavertical1](feavertical1.png)
![feavertical2](feavertical2.png)
![feavertical3](feavertical3.png)

The stress was also found to be larger than expected. In the image below is the point where the stress is concentrated the most. In order to make this smaller, we could've used a larger aluminum extrusion to make the stress concentration less.

![feavertical4](feavertical4.png)

**Floating Bearing Mount Design** (Aiden)

To design the floating bearing mount, it is 60x60mm to fit on the aluminum extrusion with a thickness of 0.25in. For the mounting hole, I made it the diameter of the set screw, which is 0.875in. There are 0.2in holes for a #10 screw. Where the bearing block and the lead screw interact, there is an RC3 fit which has a tolerance of +- 0.0005 in accordance with the handbook.

![Floating-Bearing](Floating-Bearing.png)
![Floating-Bearing1](Floating-Bearing1.png)

**Full Assembly** (Aiden)

![full-assembly](full-assembly.png)

## Bill of Materials & Labor Cost (Wyatt)
This is our bill of materials with a link to download the spreadsheet provided at the bottom of the page.

![BOM](BOM.png)

## Lessons Learned
During this assignment, our group learned about the importance of focusing on small component failure modes while designing equipment and the cost of materials is much more expensive than expected. We also learned about the importance of documenting your work because, for most of this assignment, we could reference previous work for answers.

## Links
[Motor Buy](https://www.automationdirect.com/adc/shopping/catalog/motion_control/stepper_systems/single_shaft_stepper_motors/stp-mtrac-23044)

[Motor Specs](https://cdn.automationdirect.com/static/specs/surestepACmotors.pdf)

[Motor Drawing](https://cdn.automationdirect.com/static/drawings/STP-MTRAC-23044.pdf)

[Set Screw Coupler Buy](https://www.mcmaster.com/6412K44/)

[Top Frame Corner Connectors](https://www.automationdirect.com/adc/shopping/catalog/structural_frames_-z-_rails/brackets_for_t-slotted_rails/151124-10)

[BOM](A11BOM.xlsx)

[A11 CAD and Drawings](https://drive.google.com/file/d/11uHAHFEqwJXb86kqvsGnqs_MW-SBbayR/view?usp=sharing)

## Drawings
All the drawings follow the ASME Y14.5 standards.

![MotorMountDraw](MotorMountDraw.png)
![BearingMountDrawing](BearingMountDrawing.png)
![CrossheadDraw](CrossheadDraw.png)
![A11Draw](A11Draw.png)
