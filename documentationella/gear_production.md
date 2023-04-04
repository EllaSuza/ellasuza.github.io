
[BACK TO HOME]({{ '../index.html' |relative_url }})

[Part of Hormao Machine]({{ '../index.html' |relative_url }})


I want to make a bunch of different gears that I can control through stepper motors.


### Laser cutting generic gears


### 3D printing spiral gears

### Gear pairs

##### 1

I want to make this mechanism: http://507movements.com/mm_068.html
to represent the dynamic between one day and one menstrual cycle. My average cycle is 29 days so I will be using that.

I want them to sit on my stepper motor, so that I don't need to make a component to attach them together. 

##### Step 1: Important Dimensions

Stepper motor JK42HS40-1704-83AF cylinder pin : 4.95mm diameter

Stepper motor 28BYJ-48 pin: 2.88mm x 4.87mm

Gear B # of teeth: 29
Gear A # of teeth: 1

##### Step 2: Design in Fusion

NOTES:
Backlash: 
- the defined clearance between a gear and its mating gear
- with 3d prints, you need built-in tolerances
.15mm works well with the size in the tutorial (this will end up being .3mm because we will give the same tolerance to the second gear)
- does depend on print setting

Root fillet radius:
- the higher the value, the stronger the gear teeth, but can't be larger than 1.1mm 
- you want to avoid an undercut shape of the teeth or the gear teeth will not roll smoothly off eachother

Hole Diameter:
- You can apply the center hole here, but you can also apply it later so you have more flexibility  

GEAR B:

pressure angle: 20 degrees
module: 12.7
number of teeth: 29
backlash: .15
root fillet radius: 6.588
gear thickness: 5
hole diameter: 4.95
pitch diameter: 368.3


GEAR A:

pressure angle: 20 degrees
module: 12.7
number of teeth: 29
backlash: .15
root fillet radius: 3.25
gear thickness: 5
hole diameter: 4.95
pitch diameter: 368.3


