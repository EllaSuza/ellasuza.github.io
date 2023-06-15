---
layout: default
---


[BACK TO HOME]({{ '../index.html' |relative_url }})

[Part of Hormao Machine]({{ 'documentationella/hormaomachine/hormaomachine.html' |relative_url }})

#### 3D printing
## MIDDLE FINGER JOINT AND SOCKET PRESSFIT


### FIRST ROUND:

As I mentioned before, the middle connection point between the two base faces that keeps all the components together, isn't stable enough. I want to try 3D printing this, so that the structure is more dense and not made of multiple pieces. My first test shows below:

<img src="/assets/images/calendarprototyping/midjointfit.jpg" width="300"> 

I used the same design in Fusion of the middle connection piece, and made the teeth 6mm longer in height. You can see, however, that the faces of the teeth are too wide and long. This is probably because there is little to no play in the structure of filament compared to the wood. There is also no Kerf from a laser that eats material. I think if I add a negative offset of 1mm, it will work better.


<img src="/assets/images/calendarprototyping/midjointposition.jpg" width="300"> 

In the image above you can clearly see that the position of the teeth is also completely off. I forgot that I had changed the positions in Lightburn, for a reason I cannot recall. I will have to measure the physical bases to make the connection piece allign, or recut the bases.

<img src="/assets/images/calendarprototyping/printing1/print1.jpg" width="300"> 
<img src="/assets/images/calendarprototyping/printing1/print2.jpg" width="300"> 
<img src="/assets/images/calendarprototyping/printing1/print3.jpg" width="300"> 


### SECOND ROUND:

###### DESIGN
- For this first print, I wanted to use no offset, just so I could see how strong and well the design would come out. I can then compare it to the lasercut pieces and guage how much play it will need to fit well.

<img src="/assets/images/calendarprototyping/3dcomponents.png" width="600"> _in fusion 360_

###### MAKE
Around 40% way through the job, the print would start warping and let go of the bed.
The first time I cleaned the bed better, no difference.
I then made the bed warmer (65 degrees), no difference.
I went back to Prusa slicer and added support with the paint-on support tool on the overhang (automatically generated support showed nothing), because that is about the point where it would let go of the bed. I also went from **QUALITY 0.15mm** to **DETAIL 0.10mm** in print settings.

<img src="/assets/images/calendarprototyping/printing2/midjointcomponent.jpg" width="600"> _mid joint component_

<img src="/assets/images/calendarprototyping/printing2/warpingtests.jpg" width="600"> _tests that came out warped_

<img src="/assets/images/calendarprototyping/printing2/printingwell.jpg" width="600"> _printing well_

<img src="/assets/images/calendarprototyping/printing2/printdone.jpg" width="600"> _print done_


_image of iteration 2 3d print being slightly too tight_

<img src="/assets/images/calendarprototyping/printing2/toosmallhole.jpg" width="600"> _print 2_


<img src="/assets/images/calendarprototyping/holesadapted.png" width="600"> _adapted parametrically_

<img src="/assets/images/calendarprototyping/print3/tootighthole.jpg" width="600"> _print 3_

- The hole is still a little too tight, will give it slight more play (1mm in diameter). I will wait for this until I have my lasercut components to see if the pressfit fingers need adapting as well.


