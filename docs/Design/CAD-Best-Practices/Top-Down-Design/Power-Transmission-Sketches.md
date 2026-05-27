---
icon: lucide/zap
---

# Power Transmission sketches
Power Transmission sketches are how we define dimensions pertaining to the moving aspects of the robot. This includes but is not limited to; Belt lengths, Gear sizes/ratios, and motor positioning.

!!! note "Master Sketches"

    Power Transmissions should be a part of a subsystem's master sketch *if* it directly effects position of major parts of the robot, like rollers. Otherwise, Power Transmissions should have their own sketch in the subsystem's part studio.

## Gears

Sketch Gears as tangent construction circles.
Dimension them as the number of teeth it has, divided by twenty.

!!! tip "Showing Design Intent"

    It's best to dimension a belt with the number of teeth, divided by 20, because it helps communicate design intent. Its a lot easier to tell what size gear it is if it's dimensioned as `62/20`, as opposed to `3.1`.

## Pulleys

To sketch a pulley, simply create a center point construction circle where you want a pulley to be.
Dimension the diameter as `#PulleyPD_5mm(# of teeth)`.

??? failure "Not working?"
    
    If the `#PulleyPD_5mm()` function doesn't work, double check that you have origin cube at the top of the feature tree, and "5mm Belts" is enabled.

## Belts

To sketch a belt, you must first have two pulleys defined to put the belt between.
Make two construction lines, one  on each side, tangent to both pulleys.
To make sure you get the right center-to-center distance, Dimension the center of the pulleys to each other as `BeltCTC_5mm(Belt teeth, Pulley 1 teeth, Pulley 2 teeth)`.

For example, `#BeltCTC_5mm(70,24,18)` would result in the center-to-center distance of a 70 tooth belt that runs between a 24 tooth pulley and an 18 tooth pulley.

!!! note "Belt sizes"

    Make sure to use commercially available teeth numbers or ones we have on hand, commonly multiples of 5.

!!! "Chains and Sprockets"

    To sketch Chain and sprockets, use the same method as belts and pulleys, except use `SprocketPD_25` and `ChainCTC_25` instead.

??? info "See also"

    [Gear Basics | FRCDesign.org](https://frcdesign.org/learning-course/stage1/1b/gears)  
    [Belt and Pulley Basics | FRCDesign.org](https://frcdesign.org/learning-course/stage1/1b/belts/)
    [Chain and Sprocket Basics | FRCDesign.org](https://frcdesign.org/learning-course/stage1/1b/chain/)
