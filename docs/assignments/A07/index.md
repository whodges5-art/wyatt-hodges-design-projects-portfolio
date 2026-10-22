# A7 – FEA On Bracket

## Objective
The objective of this assignment was to conduct finite element analysis on the bracket created in A5 and A6 to increase its stiffness and strength and decrease its mass while still meeting all necessary criteria. 

## Hook

### Analyze
For this assignment certain aspects of the problem are fixed and should not be changed. These constants are the material the hook and link are made of, the location and magnitude of the force being applied, and the fixed geometry of the hook and link. Once these constants are applied I can conduct finite element analysis on the parts  to improve their performance and reduce material. The material was already selected so I began by adding the fixtures and load to the hook in solid works then creating a mesh for the computer to run its simulation on.
![Fixture](applyfixture.png)
![load](applyload.png)
![mesh](applymesh.png)

Our process for conducting finite element analysis is to run a new finer mesh on the geometry until the calculated values begin to converge, once the values converge or convergence was attempted with 3 new meshes, then the values from the finest mesh are used to evaluate the design. The test for convergence is 2*|xf-xi|/(xf+xi) being less than .07 proves convergence, for this problem.   

### Decide
After running the first analysis I found that my part did not actually meet any of the necessary requirements (strength, deflection, or safety factor) for the problem and would break from this load. 
![stress1](stressmap.png)
![defl1](deflmap.png)
![SF1](SFmap.png)

After looking at the stress map I deduced the problem was the thickness of the piece connecting the cylinder to the mount, I will refer to this feature as the connector. In order to make my part meet the necessary requirements I decided to make the connector 10 times as thick to increases its strength. During the second analysis I found the hook to be strong enough to support the 800 pound load but it was not stiff enough resist deflecting more than .005 inches it also failed to meet the minimum safety factor of 4. 
![stress2](stress2.png)
![defl2](defl2.png)
![SF2](SF2.png)

In order to decrease deflection without adding material I decided to shorten the connector piece by .25 inches so there would still be a much smaller gap than before. This improved the hooks performance slightly but not enough to keep the end from deflecting .015 inches and the safety factor did not improve. 
![stress3](stress3.png)
![defl3](defl3.png)
![SF3](SF3.png)

For my next design change I decided to add a second connector piece on the opposite side of the mount to support the hook, while doing this I needed to increase the length of the cylinder so it would be able to support the .75 inch thick u-line strap. After adding this feature my hook met all the necessary criteria with a max stress of 8593 psi in the connector above the cylinder, a max deflection of .003547 at the bottom tip of the cylinder, and a minimum safety factor of 4.455, and the hooks mass was .44 pounds. 
![stress4](stress4.png)
![defl4](defl4.png)
![SF4](SF4.png)

## Link

### Analyze
The link that was design for A5 and A6 was meant to slide onto the hook and have a cylindrical hole at its other end so something could be fastened to the hook. Given that description when conducting FEA the hole meant to connect to the hook will be fixed and the other hole will receive the load.
![linkfea](linkloadfix.png)

### Decide
After conducting the first finite element analysis I found the link to work correctly but the safety factor was 2.795 which is less than desirable so to increase the links safety factor I increased its thickness. 
![stress5](Stress5.png)
![defl5](defl5.png)
![SF5](SF5.png)

The FEA for this produced almost identical results just with larger numbers on the graphs including a minimum safety factor of 6.447. Since my product was working correctly I now wanted to reduce its weight without increasing stress or strain which could be done by shortening the link but I decided to remove the area of the link under the most stress so it would be distributed across portions that are carrying less stress. 
![designchange](Design change.png)

After conducting the FEA on this design I found it to be slightly less stiff and strong but was able to reduce its weight by about 20%. 
![stress6](stress6.png)
![defl6](defl6.png)
![SF6](SF6.png)

After the final design the link had a max stress of 9672 psi at the bottom of the sides of the added slot, a max deflection of .002876 in the area between the bottom hole and the slot, a safety factor of 4.124, and a mass of .21 pounds. Before adding the slot the max stress occurred at the sides of the hole with the applied force and max deflection occurred at the bottom of the same hole.

## Communicate
During this part of the assignment I learned how read stress and deflection maps effectively and the best practices for removing stress and strain by either adding or removing material and when each should be applied. If the material is not stiff or strong enough it is best to add more material to its cross-sectional area. If the material is able to meet the requirements it is best to remove material where there is high stress so it can be distributed under areas with little stress. 
