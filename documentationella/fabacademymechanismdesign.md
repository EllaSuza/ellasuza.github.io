---
layout: default
---

[BACK TO HOME]({{ '../index.html' |relative_url }})


# Fabacademy week


## NOTES LECTURE:

Assignment:
- an automation to control a sequence of operations and some kind of application

- think of a machine
design the mechanical part
move the machine by hand before you add motors to it
build a group page, describe what you did

- automation



Machine = mechanism
- a way to actuate it




- rapid prototyping of rapid prototyping

two topics:

- mechanism
- automation


- stress and strain
- when you apply stress on a material, strain is the relative response to it

- different levels to this, and we want to stay within the LINEAR range where we don't permanently damage the material

'stiffness is the slope of stress'
'strength is the how far you can push a material before it fails'

- if you make a structure, you have degrees of freedom and areas of constraints


- friction is important (material against material)


- you dont want a machine to have a differentp position when you go forward or backward - effort goes into fighting HYSTERISIS

- force loops

- kinematic coupling
    - add and remove things
    - looks simple but is not
    micron resolution

to make a machine you :

- need to pick a material

rubber/foam for damping
garolite: stiffer

avoid wood for machine builfing,because it responds to humidity

washers put some elastic force on nuts and bolts
rivets for a lot of joints
magnets are easily removeable
drives are how you get forces distributed / transmits the forces


- gear design is surprisingly subtle
    - many types of gears
    - you dont want the teeth to slash against eachother
    - involute gears are most common


planetary gears : for reduction

 to transmit forces and machine is to use belts
 - flexible in a transverse axis but you can't stretch them
- need a sprocket

- capstan drive can be a good constraint and useful to transmit forces
- thread as well


- chains are used when you want to transmit way bigger forces

- harmonic drive is a metal ring and an asymmetric cam
- inner and outer ring differ by # teeth


- couplers
very stiff rotationally
but angular freedom


- before you automate a machine, manually work it 


ball bearings
thrust bearings
linear bearings

pillow blocks are a deformable material you move against

skateboard bearings
- very competitive, and affordable because produced so much


bearing wheels in combo with a flexible carriage
- beehive linear axis

bearings
- very cheap to buy, best not to 3D print


Omnibot
- wheels that can go in multiple directions

ROUTING CABLES
- cable ties to hold bundles together, or Hook and loop

MECHANISMS
- how you build systems out of the above building blocks

SETTING FORCE NOT POSITION : SERIES ELASTIC
- your muscles dont set positon they set force of your leg, and you vary that
- by pushing through a spring (pushing first spring which then pushes leg) you can make a smoother motion


PANTOGRAPH
- small motion from big motion and vice versa

COREXYZ
- fixed motion whilst creating movement on 3 axis
- reduces moving mass

#### AUTOMATION




## NOTES FABLAB PRESENTATION:

what is a machine?
- EU machune directive 2006/42/EC

an assembly
a device that uses power to perform actions to achieve tasks


basic components of a machine
- structual components
- mechanism
- actuators (power source)


- important to structure the machine

Functional Breakdown Structure
    - ehat does it have to do
    - what functionality do you need for that
    - which functions can be combined and which have to be seperated


Product Breakdown Structure
    - what does it look like
    - what components are needed


## MECHANICAL PRINCIPLES

- making movements out of other movements or combined movements


for stability
- arrange the bearing surfaces such that if one surface (or contact point) is removed, the degree of freedom is perpendicular to that surface

- kinematic coupling

- overdetermined
when there is an excess of contact points
a 4-legged table for example
really think about what is needed


(in)accuracy

- play/hysteresis
- stiffness
- error chain and force loops
- shapes
    - perpendicularity
    - flatness
    - parallel
    - symmetry
- position


- resolution vs accuracy

resolution = ability to show or produce details

accuracy   = ability to be correct or exact
- defined by more than just the resolution


## MOVEMENT CONTROL

- cam-followers
- slot-followers


- linkage mechanisms

- step sequence control
    - step design
    - components
    - time in a discrete way


TIPS
- spiral design

