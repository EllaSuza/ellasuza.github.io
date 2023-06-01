---
layout: default
---

[BACK TO HOME]({{ '../index.html' |relative_url }})


# Full Spectrum Laser

Learn, one of the departments at Waag, also has a lasercutter. We are giving a workshop on how to use it in May, so on this page I will document the highlights of its manual and how to work with its software.

BED:
50cmx30cm


Carton planken
95cmx115cm



## SET UP at machine

water pump system
ventilation
air pump
laptop safely

then turn it all on

## FROM DESIGN TO CUT
an overview of the steps to take to go from a design in Retina Engrave 3D to the post-cut process.


#### 1. Open **RETINA ENGRAVE 3D** 
- the first time you open it up, it will ask you to select the laser in a popup menu.
- If the connection dialog shows the laser as disconnected, make sure the Ethernet or USB cable is plugged in and power cycle the laser. In the bottom left corner, click on RECONNECT to apply.

#### 2. Print from any application and select the FULL SPECTRUM ENGINEERING DRIVER

- it accepts the following file formats:



- you can also design something in Retina Engrave.

#### 3. Design View

In the top left, there are tabs to control the design space; RASTER ENGRAVE, VECTOR CUT, DESIGN VIEW, and 3D ENGRAVE. When you open up Retina Engrave, it will be in DESIGN VIEW.

- design your desired outcome. When ready, click on **RENDER** in the left panel. A pop-up should show the program preparing it. 

- Use the **Control Panel** on the right to adjust the power and speed of the job.


#### 4. Choose MODE: Vector cut or Raster engrave
- click on the mode tab that corresponds to the type of job you would like to perform.

- In the top panel, make sure the MODE corresponds with what you are doing.

For engraving:
- the engraving areas should be black.

For cutting:
- colours including Black, Red, Green, Blue, Magenta, Cyan, Yellow, all correspond to individual paths and settings. These can be established in the **vector layers** of the **control panel** on the right. 

> ##### Good to know!
> for cutting cardboard of 2.8mm thickness:
>
> Power 30, Speed 20, Pass 1 works well
> same for Power 50, Speed 100 

>For engraving cardboard of 2.8mm thickness:
> Power 30, Speed 100 
>
> for cutting paper:
> Power 10, Speed 100 = good (no burn marks unless gone over area multiple times)
> 
> for rastering on paper:
> Power 10, Speed 100 = nothing happening
> Power 20  Speed 75 = good, (no burn marks)
> 

> for cutting thick paper:
> 
>
>




#### 4. Start cutting

- Run the job perimeter, to make sure that your design will fit on your material. You do this by clicking the button with four arrows pointing to its corners in the top panel.

- Press the **GO** button, this will download the job to the laser's temporary memory and starts it. 



## GOOD TO KNOW

We have a laptop available with the lasercutter. It is possible to connect the machine to a computer either using an ethernet or USB cable. This is required for the lasercutter to download jobs, and once there is a loss of power the machine will not remember previous jobs. We use a USB connection.

SETUP
before you turn on the laser, the water pump, ventilation, and inside air pump needs to be connected and turned on 

WATER PUMP
- tube from the pump goes to IN
- loose tube in water goes to OUT

### 1. Retina Engrave 3D

The laptop available already has this software installed. If this is not the case anymore or you are using your own laptop, see the manual on how to install through just a couple of steps. <a href="https://info.fslaser.com/hubfs/Public_Documents/RetinaEngrave%203D%20Manual.pdf" target="blank" rel="noopener noreferrer" >see here </a> 

### 2. CONTROL PANEL INTERFACE

##### GOOD TO KNOW:
- The laser system is controlled by the 3D PRO controller. This performs allignment and testing without the need of a PC connection. The LCD touch panel also allows you to control these.
- Using a microSD card, you can permanently store jobs that have been created in the RetinaEngrave software, on the laser.


#### Starting a job

- once you have a job that has been prepared in RetineEngrave, face the LCD touch panel:

1. Press the MODE SELECT button that reads **FS/Z** until the MODE field reads **'FF'**

2. The SELECTION field should then rewad **'filename.bin'** where the 'filename' is the name of your made job.

3. Press the **START/CANCEL** button to load the job.

4. Press the **START/CANCEL** button again to start the job.


* * *



## PANEL AND DISPLAY specifics


##### Diagram of LCD screen and control panel

<img src="/assets/images/fullspectrum/diagram%20fullspectrumlaser-01.png" height="800"> 

##### USE OF BUTTONS during setup

###### 1. FS/Z (MODE SELECT)
a. Toggles between the different modes
b. Fast XY Jog (Mode 0) -> Slow XY Jog (Mode 1) -> Alignment (Mode 2) -> File Select (Mode 3) -> Factory Reset (Mode 4)

###### 2. LOCK/UNLOCK
Locking or unlocking the drive motors. The system cannot jog or test fire whilst unlocked, but it does allow for the laser head to be positioned by hand.

###### 3. HOME
a. When in **FAST XY** (Mode 0) or **SLOW XY** (Mode 1) this button will get the laser head to seek the home position. After this, it will know its position. When you unlock the motion system the position is forgotton so you need to **rehome**.

###### 4. RETURN/TEST FIRE
a. In **Fast XY** (Mode 0) or **Slow XY** (Mode 1) the laser will move to the previously saved job start position.
b. In **Alignment** (Mode 2) this button fires a short-duration pulse designed to mark thermal paper.

###### 5. RUN PERIMETER
a. In **Fast XY** (Mode 0) the bounding perimeter of the job will be shown quickly (RetinaEngrave software must be started/loaded with a job for this function to be active).
b. In **Slow XY** (Mode 1) the bounding perimeter of the job will be shown slowly.

###### 6. START/CANCEL
a. In any menu mode (File Select or Factory Reset) this button will select the option displayed in the **SELECTION** field.
b. Cancels a move operation (homing, autofocus or a running job).
c. In **Fast/Slow XY**, with the laser UNLOCKED, this fires a higher-power test pulse.
d. In **Fast XY**, pressing this button after the laser homes will rapidly move the head to the upper left corner of the workspace.
e. In **Slow XY**, pressing this button after running a job will allow you to re-run the same job.

###### 7. JOG BUTTONS (4 arrows)
a. In **Fast/Slow XY** (Modes 0 and 1), the buttons move the laser head left/right and front/back.
b. In **File Select** (Mode 3) the up and down buttons scroll through the loaded jobs.


##### Details

- the POWER field displays the laser current in mA. Anything less than 2mA is considered off.

##### USE OF BUTTONS during a job

Only the LOCK/UNLOCK and CANCEL buttons function. All other function buttons are disabled.

###### 1. LOCK/UNLOCK
a. LOCK/UNLOCK pauses/resumes the job.
b. CANCEL cancels the job.

###### 2. UP/DOWN JOG BUTTONS 
allow you to adjust the job power on the fly. Scale is from 0 (**no power**) to 255 (**full power**).

