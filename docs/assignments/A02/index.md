# A2 – Truss Stress Analysis

## Objective
The Objective of this assignment is to design and create a a 3D model of a truss and learn the steps of the design process involved. 

## Analyze
![Problem](TrussProblem.png)

The truss needs to be able to support the 2 loads, which I chose to be equal to 20 kN. The distance between the members are given in vertical and horizontal distances and can be used to break forces into their x and y directions. A is a pin so it will have a vertical and horizontal reaction force. B is a roller so it will have a vertical reaction force.  

## Decide
I started my decision making process by sketching different ways to connect these 4 points making a truss. The three ideas i came up with were connecting points C and A, connecting points D and B, and connecting C and D to a midpoint on AB to create a symmetrical truss. 

![Decision](A2Decision.jpeg)

I originally decided to connect points C and A because then most of the reaction forces would be in pin A, but after I started drawing a free body diagram I realized there would be more forces acting at A than anywhere else so I decided on the one that connects points B and D to make the math simpler. 

![FinalDecision](A2FinalDecision.jpeg)

## Communicate

After deciding how I was going to design the truss the next step was to solve for the internal loads of the beams. The first step was drawing the free body diagram for each joint and symbolically solving for the unknown internal loads. This was done by setting all forces in the x and y directions equal to 0 then and using the ratio of vertical/horizontal distance to break down forces that do not lie on those axis.

![FBD1](A2FBD1.jpeg)
![FBD2](A2FBD2.jpeg)

After solving for the values symbolically I was able to get all the internal forces in terms of P, a, b, d1, and d2 which are given (d1=sqrt(a^2+b^2) and d2=sqrt(4a^2+b^2)) and solve numerically.

![Fsolved1](A2Fsolved1.jpeg)
![FSolved2](A2FSolved2.jpeg)

After finding the internal loads the next step is to determine the size of the beams necessary to support the loads and the weight of the truss. The problem said the truss would be made of A 500 structural steel with uniform area so I used a table on https://beamdimensions.com/materials/Steel/ASTM/ASTM_A500/ to find its properties, the safety factor is 3.5 and the largest internal load is 37.97 kN. There were multiple values dependent on the grade, I decided A is probably cheapest and used those table values for yield strength and density. The first step in this process was to symbolically solve for the minimum cross section area (we already did it in class so that step is at the bottom of the page), then plug in my values and numerically solve for it. For the force I used the largest internal load, because this member is most likely to break. To determine the weight of the truss the equation is area * length * density * gravity constant. Because all the members have the same area, density, and gravity constant I solved this by plugging the total length of all the beams into the equation rather than finding the weight of every beam. 

![BeamSize](A2BeamSize.jpeg)

The final step in solving this problem is to determine the necessary size of the pins that will be holding the truss together. First I had to find the pin that would have the greatest shear force applied to it. I did this by drawing a free body diagram for each pin with equal and opposite forces pushing along the axis. The values of the forces were determined by which ones were acting solely in the positive/negative x and y direction and knowing the opposite equilibrium force would have an equal magnitude. 

![ShearFBD](A2ShearFBD.jpeg)

Yield shear strength, safety factor, and density were all given so I solved the shear stress equation for area symbolically. the value for yield strength was in incorrect units so I first used google to convert my value to correct units then plugged in my numbers and numerically solved for the cross sectional area. 

![PinSolved](A2PinSolved.jpeg)

After finding area the final task was to find the weight of all the pins combined. This used the same equation as the weight of the beams the only value I didn't have was the length of the pins so I googled how long a truss pin is and I found an equation for slenderness ratio that says the pin should be no more than 3 times as long as the its diameter, in this case the length should be less than 3.99 cm. After finding that value I was able to find the weight of 1 pin I then multiplied that value by 4 because there will be 1 pin at each joint. 

![PinWeight](A2PinWeight.jpeg)
