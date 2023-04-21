---
layout: default
---


[BACK TO HOME]({{ '../index.html' |relative_url }})

[Part of Hormao Machine]({{ '../index.html' |relative_url }})


# Calendar with cyclical variables

I wanted to create a calendar with replacable components so that I could use the same structure for tracking multiple things. The first idea I had was to have multiple movable circles held together, working similarly to a compass. I first made it out of carboard and laser cutting it.

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

I made the two sides of the base slightly longer to be able to show more data, and wider so that certain parts wouldn't be as fragile. I haven't cut the circles out of wood yet, because I want to design the representation of data first so I can engrave on it right away. I used the cardboard versions to see if the dimensions still work.

![prototype1calendar](/assets/images/calendarprototyping/calendarcyclical.mp4)


I then used the graph I had made, [more info on that here]({{ '../index.html' |relative_url }}), and applied it to the structure in Illustrator.

![data representation applied to prototype](/assets/images/calendarprototyping/dataonprototype.png)

<img src="/assets/images/calendarprototyping/3.jpg" width="600"> 




- And it moves really smoothly! The pressfit connections were initially really sturdy, but they gradually became not so sturdy. I wonder if these were thicker and therefore less prone to fall out of their pockets on the their base, it would work better. I could glue all of it together permanently, but I really want the components to be replacable and adaptable by the user, as well as easily assembled.


<img src="/assets/images/calendarprototyping/1.jpg" width="300"> 

<img src="/assets/images/calendarprototyping/4.jpg" width="300"> 

<img src="/assets/images/calendarprototyping/5.jpg" width="300"> 

<img src="/assets/images/calendarprototyping/6.jpg" width="300"> 

<img src="/assets/images/calendarprototyping/7.jpg" width="300"> 

##### Engraving settings:


- The engraving did not turn out well. I tried a couple of different ratios between power and speed, but the outcome also kept changing. A couple of days later the laser lens was cleaned and turned out it was really dirty, so perhaps that was the problem. I also looked at some pieces the other intern Maria had done with text engraving, and in image mode text came out really nicely. I might try that instead of fill or line mode.




# Clock charged by gears

<a href="https://www.instructables.com/Laser-cut-gear-clock-with-Chronodot/" target="blank" rel="noopener noreferrer" >instructables basis </a> 


- Cut their svg file in lightburn, because I couldn't figure out how they made the gears work with eachother.

#### ASSEMBLY

- I am using a different stepper motor than in the instructables, so will have to adjust the size of the hole in the gear that attaches to the motor pin. 

Stepper motor 28BYJ-48

- pin: 2.88mm x 4.87mm


Drilling was not an option (gears were way too fragile) so I recut them with new fitting holes. I tried a couple of different dimensions because I want the gear to sit tightly on the motor pin:

<img src="/assets/images/motor1.jpg" width="300"> 



(image of different sized holes in gears)

