---
layout: default
---


[BACK TO HOME]({{ '../index.html' |relative_url }})

[Part of Hormao Machine]({{ 'documentationella/hormaomachine/hormaomachine.html' |relative_url }})

# Calendar with cyclical variables

<img src="/assets/images/calendarprototyping/workchaos.jpg" width="800"> 


I wanted to create a calendar with replacable components so that I could use the same structure for tracking multiple things. The first idea I had was to have multiple movable circles held together, working similarly to a compass. I first made it out of carboard and laser cutting it.


## PROTOYPE 1 : cardboard

#### The cardboard I used : 2.5mm

#### DESIGN IN FUSION

<img src="/assets/images/calendarprototyping/calendarinfusion.png" width="600"> 


#### The cutting settings I used in Lightburn
speed: 80

power max: 75

power min: 20



<img src="/assets/images/calendarprototyping/calendar1.jpg" width="500"> 

This shows one side of the base structure, with the circles held in place by supportive arcs glued to the base. It was all pretty sturdy, except for the teeth of the pressfit middle connection pieces. When I applied pressure to the teeth to press it into the holes on the base, they would crumble like below. 

<img src="/assets/images/calendarprototyping/calendar4.jpg" width="500" height="500"> 

I then grabbed some scrap thicker cardboard and cut the teeth out of that instead. It looks similar to MDF in structure but is definitely still cardboard. It is luckily the same thickness. Below is what this looks like once glued to the middle connection base. : s40 p95 works for this material with the laser.

<img src="/assets/images/calendarprototyping/calendar3.jpg" width="500" > 

(pressfit connection pieces)


<img src="/assets/images/calendarprototyping/calendar2.jpg" width="500"> 

The structure was surprisingly sturdy, although not for long. The circles were able to move quite easily,so I felt I could keep the dimensions of them as well as the supporting arcs the same.


## PROTOYPE 2 :

I made the two sides of the base slightly longer to be able to show more data, and wider so that certain parts wouldn't be as fragile. I haven't cut the circles out of wood yet, because I want to design the representation of data first so I can engrave on it right away. I used the cardboard versions to see if the dimensions still work.

![prototype1calendar](/assets/images/calendarprototyping/calendarcyclical.mp4)


I then used the graph I had made, [more info on that here]({{ 'documentationella/hormaomachine/hormaomachine.html' |relative_url }}), and applied it to the structure in Illustrator.

![data representation applied to prototype](/assets/images/calendarprototyping/dataonprototype.png)

<img src="/assets/images/calendarprototyping/3.jpg" width="600"> 

![prototype2calendar](/assets/images/calendarprototyping/calendarAnxietydata.mp4)


- And it moves really smoothly! The pressfit connections were initially really sturdy, but they gradually became not so sturdy. I wonder if these were thicker and therefore less prone to fall out of their pockets on the their base, it would work better. I could glue all of it together permanently, but I really want the components to be replacable and adaptable by the user, as well as easily assembled.

- After a couple of days, some of the teeth on the pressfit middle connection broke off, and although it clicks together well it doesnt hold it long. I wonder if longer teeth would be helpful, or perhaps printing it out of filament so the teeth and base are one component.



<img src="/assets/images/calendarprototyping/1.jpg" width="300">  <img src="/assets/images/calendarprototyping/4.jpg" width="300"> <img src="/assets/images/calendarprototyping/5.jpg" width="300"> <img src="/assets/images/calendarprototyping/6.jpg" width="300"> <img src="/assets/images/calendarprototyping/7.jpg" width="300"> 

##### Engraving settings:


- The engraving did not turn out well. I tried a couple of different ratios between power and speed for the text, but the outcome also kept changing. A couple of days later the laser lens was cleaned and turned out it was really dirty, so perhaps that was the problem. I also looked at some pieces the other intern Maria had done with text engraving, and in image mode text came out really nicely. I might try that instead of fill or line mode.
- The circles engraved are also quite irregular, perhaps the speed was too high for the laser to manage.

View [Our lasercutter]({{ 'documentationella/lasercutter.html' |relative_url }}) page for more information on settings and options



## PROTOTYPE 3: The cycle watch/bracelet

I want to make the calendar wearable, and therefore more compact and sturdy. I am building off of the previous designs.
Because I am going to be 3d printing and lasercutting components that need to fit together, I need a clearer work flow so that measurements don't get lost along the way.
- Design the structure in Fusion 360
- Export lasercutting components as dxf
_ Export 3d components as obj/stl
- Import finished dxf design to Illustrator, and apply graphics
- Import obj/stl to slicer for printer


DON'T GO BACK AND FORTH!! (you screw yourself over ella)

- Any necessary adaptations
    - Choose material to lasercut and if needed go into fusion to adapt parameter
    - 3d printed middle connection piece outcome compare to bolts 

    - go back to fusion to make needed changes

> #### GOOD TO KNOW
> In fusion360, if you copy and paste a component it will automatically stay linked to the origin component. So if you make changes this will directly do so to the origin component as well. In order to avoid this, When pasting. choose PASTE NEW.


### DESIGN THE STRUCTURE IN FUSION 360


<img src="/assets/images/calendarprototyping/watchinfusion1.png" width="600"> _without top base_

<img src="/assets/images/calendarprototyping/watchinfusion2.png" width="600"> _with top base_

- I made a couple of parameters:
offset of joint for middle pressfit connection
thickness of wood for lasercutting
diameter of hole for bolts

- Next time I do this, however, I will make the whole design parametrically put together. This will make it a lot easier to make small changes as well as work towards the larger picture of my project which is for these tools to be adaptable for different people.

### EXPORT LASERCUTTING COMPONENTS AS DXF

### EXPORT 3D COMPONENTS AS OBJ/STL

top connection base to base
middle connection base to base
bottom connection base to base

[page on process of 3D printing components]({{ 'documentationella/hormaomachine/watch_3dcomponents.html' |relative_url }})

### IMPORT FINISHED DXF DESIGN TO ILLUSTRATOR AND APPLY GRAPHICS


<img src="/assets/images/calendarprototyping/watchinillustrator.png" width="600"> _imported_



##### creating graphs out of my collected data of cycles 2, 3, and 4 of the year 2023
<img src="/assets/images/calendarprototyping/line-graph.png" width="600"> _cycles 2, 3, and 4 of 2023_

<img src="/assets/images/calendarprototyping/line-graph-2.png" width="600"> _design to create_



### ANY NECESSARY ADAPTATIONS

- Material thickness of wood for lasercutting: 4mm
- mid connection piece socket way too small for bolt


- Went back to Fusion360 and:
    - realized it didnt make it match the bolt so adapted the parameters
    - extruded the connection pieces 2mm more
    - exported one as a test
    - back into slicer
    



RESEARCH ON DATA HORMONES

https://www.ncbi.nlm.nih.gov/books/NBK279054/#:~:text=Estrogen%20levels%20rise%20and%20fall,end%20of%20the%20menstrual%20cycle.

https://womeninbalance.org/about-hormone-imbalance/

https://www.news-medical.net/health/Estradiol-Measurement.aspx

