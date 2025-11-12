---
title: "Multimaterial Pliers"
excerpt: "These 3D printed pliers use rigid and flexible components."
header:
  image: /assets/img/pliersFusion.png
  teaser: /assets/img/pliersFusion.png
gallery:
  - url: /assets/img/before1.png
    image_path: assets/img/before1.png
    alt: "before"
  - url: assets/img/after1.png
    image_path: assets/img/after1.png
    alt: "after"
 
---
### Print-in-Place Pliers

![pliers gif](/assets/img/PliersGIF (1).gif)

### About the Design
For my assignment, the objective was to filament print pliers capable of gripping and picking up through-hole resistors. 
The requirements are that the pliers return to the open position when not in use, and they have to be assembled 
by hand using no tools.

I modeled my design after the design in the 2017 [article by Bulent Yusef](https://all3dp.com/3d-printed-flexible-pliers/). 
For the handles and jaws, I used PLA filament. For the flexible centerpiece I used 95A TPU and a grid pattern with 0.75 mm 
wide lines. I found this to be the perfect balance of flexibility and durability for the spring component of the pliers. 
It’s connected to the rigid handles and jaws with an interlocking pattern that fits together tightly (shown below). 

![Interlocking pattern](/assets/img/puzzle.png)

### Specifications
The jaws are 60 mm long and have a capacity of 10.5 mm, meaning they can open up to 10.5 mm wide. This is very practical for my objective of picking up through hole resistors.


### CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH90d2dQT28d5b6028113a1bb0309612c4f6?mode=embed" width="800" height="600" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>


###Iterations
{% include gallery caption="Before and after adjusting closure angle for a better contact between jaws." %}

### Print Settings
For this print, I used a 0.6 mm nozzle, so the layer height for the print is 1.2 mm. For the spring component in the center of the pliers, I used 95A TPU. For the rigid parts, the jaws and handles, I used PLA. I used a 25% infill density for all of the parts. 
