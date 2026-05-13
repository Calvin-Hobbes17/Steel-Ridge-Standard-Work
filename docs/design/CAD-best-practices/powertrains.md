# Powertrains
Powertrains are how we define dimensions pertaining to the moving aspects of the robot. This includes but is not limited to; Belt lengths, Gear sizes/ratios, and motor positioning.
Powertrain sketches should be a part of a subsytems mastersketch **if it directly effects position of major parts of the robot**, like rollers. Otherwise, Powertrains should have their own sketch in the subsystems part studio.
## Defining Pulley sizes
To sketch a pulley, simply create a construction circle where you want a pulley to be. To define it first make sure you have an origin cube in your part studio. Then, use the dimension tool and type #pulley. A function that reads #pulleyPD5mm() should appear in small menu. 
After clicking on #pulleyPD5mm(),type the number of teeth you want in between the parenthesis. **Note:** Make sure to use commercially available teeth numbers or ones we have on hand, commonly 15, 18, and 24. 
#pulleyPD5mm(24) would result in the diameter of a 24 toothed pulley.
