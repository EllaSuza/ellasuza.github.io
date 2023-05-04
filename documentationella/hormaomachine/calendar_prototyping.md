---
layout: default
---


[BACK TO HOME]({{ '../index.html' |relative_url }})

[Part of Hormao Machine]({{ 'documentationella/hormaomachine/hormaomachine.html' |relative_url }})


# Calendar with cyclical variables

I wanted to create a calendar with replacable components so that I could use the same structure for tracking multiple things. The first idea I had was to have multiple movable circles held together, working similarly to a compass. I first made it out of carboard and laser cutting it.


## PROTOYPE 1 : cardboard

#### The cardboard I used : 2.5mm

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


I then used the graph I had made, [more info on that here]({{ '../hormaomachine/hormaomachine.html' |relative_url }}), and applied it to the structure in Illustrator.

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


## Middle finger joint pressfit
#### 3D printing

As I mentioned before, the middle connection point between the two base faces that keeps all the components together, isn't stable enough. I want to try 3D printing this, so that the structure is more dense and not made of multiple pieces. My first test shows below:

<img src="/assets/images/calendarprototyping/midjointfit.jpg" width="300"> 

I used the same design in Fusion of the middle connection piece, and made the teeth 6mm longer in height. You can see, however, that the faces of the teeth are too wide and long. This is probably because there is little to no play in the structure of filament compared to the wood. There is also no Kerf from a laser that eats material. I think if I add a negative offset of 1mm, it will work better.


<img src="/assets/images/calendarprototyping/midjointposition.jpg" width="300"> 

In the image above you can clearly see that the position of the teeth is also completely off. I forgot that I had changed the positions in Lightburn, for a reason I cannot recall. I will have to measure the physical bases to make the connection piece allign, or recut the bases.

