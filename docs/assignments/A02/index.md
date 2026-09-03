# A2 – Truss Stress Analysis

## Objective
The Objective of this assignment is to design and create a a 3D model of a truss and learn the steps of the design process involved. 

## Part 1 Design Truss

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
