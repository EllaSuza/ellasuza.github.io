---
layout: default
---

[BACK TO HOME]({{ '../index.html' |relative_url }})


# Fabacademy OUTPUT devices 
NOTES

INPUT - system - OUTPUT


###### LAMP:
- glowing filament in a near-vacuum glass case
- don't use them (inefficient with energy)

###### LED:
- Light-emitting Diode
-colour depends on the materials used

- Focused beam
- forward voltage depends on the used material
    - check the datasheet

you need to know the forward voltage to calculate the necessary resistor

- Driving one LED from one uC pin?
You connect directly through a resistor

- Driving more LEDs from one pin?
You connect through a MOSFET or BJT
External power

Mosfet controls the power going through
- Mosfet is a transistor


###### LED - RGB discrete
- multiple coloured LEDs in one case
- controlled by PWM pulses


SPEAKERS
- solenoid attached to a membrane
- 20Hz-20kHz

###### MOTOR - DC

- gate (you control through gate)
- drain
- source

- through PWM, so you can control speed
- can become very hot

###### MOTOR - SERVO

DC motor + gearbox + sensor = position control
- via een feedback loop via de sensor


- location is controlled via analog voltage (PWM)

limitations:
- dont rotate continouosly 
- works with fixed angles


###### MOTOR - STEPPER

- can not remember where it is, which is why it will always go to home before go to new spot

- can control angle without feedback loop


