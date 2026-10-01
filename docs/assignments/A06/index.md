# A6 – Bracket Drawing

## Objective
Create a model and an effective engineering drawing of the bracket from A5

## Analyze
To model this I need to create equations in the table to link features that are dependent on each other. I first needed to decide if I was going to us the stress or deflection equations I used deflection because those values required larger values for my unknown dimension.

## Decide
I already had all my equations and known values from the last assignment so I began with entering my known values into the table and then used the same process I did in my paperwork last week with my computer. I first solved for the hook diameter which gave me a value for feature 2's width so I could solve for thickness and length. Then I had found last week that the thickness dimension of features 3, 4, and 5 is equal so I was able to put terms in relation to thickness. I also found that feature 4 had a fixed dimension size and would affect the dimensions of feature 3 and 5. I then input my equations with the correct variables to find all the correct dimensions For the link I used the necessary area to find the necessary length then was able to find a relationship between its thickness and width so I set the width to a 2*diameter of the rod because that would leave more material between the holes and the edge. I could then use this value to find the thickness and change the width value if necessary. 

## Communicate
The equation I used to drive the diameter of the hook was the stiffness equation because it required me to have a larger diameter which would also satisfy the strength equation. I was able to do this by inputting known values that come from material property and are given in the assignment and then typing those variables into the property table to equate them to the diameter. If I were to change this value the values for feature 2 would also change in the equation table, but even though I referenced the global variables while dimensioning my part the model did not change in size until I edited the dimension to reference the variable again.

I changed the tolerance of the thickness of the top features to be only positive because all of those features would be more likely to fail if that value is smaller and would all get a little stronger when the value is larger. I also made the tolerance for the height of the T smaller because if it gets too large it would be too loose around the mount and slide off. 

This assignment was helpful for learning how to apply tolerances to solid works drawings by using things like the equation table and built in tolerance functions. Dimensioning and tolerance help communicate design intent because it shows how these parts can fail easily and what dimensions are most important to ensure a successful design. This assignment took me about 6 hours to complete.
Attached below are my CAD models and drawings as well as images
