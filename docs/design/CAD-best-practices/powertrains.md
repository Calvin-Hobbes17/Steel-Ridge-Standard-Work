---
icon:lucide/zap

# Powertrains
Powertrains are how we define dimensions pertaining to the moving aspects of the robot. This includes but is not limited to; Belt lengths, Gear sizes/ratios, and motor positioning.
Powertrain sketches should be a part of a subsytems mastersketch **if it directly effects position of major parts of the robot**, like rollers. Otherwise, Powertrains should have their own sketch in the subsystems part studio.

## Pulleys

#### Sketching pulleys

To sketch a pulley, simply create a center point construction circle where you want a pulley to be.

#### Defining pulleys

To define it first make sure you have an origin cube in your part studio. Then, use the dimension tool and type #pulley. A function that reads /#pulleyPD5mm() should appear in small menu. 
After clicking on #pulleyPD5mm(), type the number of teeth you want in between the parenthesis. 
/#pulleyPD5mm(24) would result in the diameter of a 24 toothed pulley.

**Note:** Make sure to use commercially available teeth numbers or ones we have on hand, commonly 15, 18, and 24. 
## Belts
#### Sketching a belt
To sketch a belt, you must first have two pulleys defined to put the belt between. Make a construction line that is coincident to the center of each of the pulleys. Make two more construction lines, one  on either side of the center line, and make them each tangent to both pulleys.
#### Defining Belt lengths
To dimension a belt first make sure you have an origin cube in your part studio. Then use the dimension tool on the **center** line between the pulleys. Similar to dimensioning a pulley, type #Belt and select #beltCTC_5mm()
In between the parenthesis, make sure to add three numbers seperated by commas. The first number is the amount of teeth you want your belt to have, and the second and third numbers are the amount of teeth the two pulleys the belt runs between has.
For example, #beltCTC_5mm(70,24,18) would result in a 70 tooth belt that runs between a 24 tooth pulley, and an 18 tooth pulley.

**Note:** Make sure to use commercially available teeth numbers or ones we have on hand, commonly multiples of 5.
#### CADing belts
First, ensure you have the Belt & Chain Gen featurescript, found [here.](https://cad.onshape.com/documents/53c0b14cad92676c14e04e97/w/1271c254ccb0a79563210195/e/7394c4a86d8d6c35c9a12041)

Open the featurescript in your part studio, and select the two pulleys the belt is dimensioned to. Double check that the width is 9mm, and the pitch is HTD5mm, and hit check. Don't worry about offsets. These are parts that you will insert into your assembly later.
## Gears
#### Sketching Gears
A simple process very similar to pulleys. Create a center point construction circle everyplace you need a gear. If you want the gears to be connected, make sure your circles are **tangent** to eachother.
#### Defining Gears
To define a gear, use the dimension tool and type the amount of teeth you want the gear to have, then divide that number by twenty.
For example, 64/20 would result in the diameter of a 64 tooth gear.
