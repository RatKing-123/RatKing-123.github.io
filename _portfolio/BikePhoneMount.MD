---
title: "Bike Phone Mount"
excerpt: "Mount your phone to your bike - and rotate it!"
header:
  image: /assets/img/bikemountrender.png
  teaser: /assets/img/bikemountrender.png
gallery:
  - url: /assets/img/enclosure.png
    image_path: assets/img/enclosure.png
    alt: "enclosure"
  - url: assets/img/lid.png
    image_path: assets/img/lid.png
    alt: "lid"
  - url: /assets/img/motormountingplate.jpg.png
    image_path: /assets/img/motormountingplate.jpg.png
    alt: "motor mounting plate"
  - url: /assets/img/carriage.png
    image_path: /assets/img/carriage.png
    alt: "carriage"

  - url: /assets/img/end support.png
    image_path: /assets/img/end support.png
    alt: "end support"

  - url: /assets/img/syringesupport.png
    image_path: /assets/img/syringesupport.png
    alt: "syringe support"


---

### Top-Down Modeling

Top-down modeling is an approach in design where you start with the overall concept or higher-level features of a product and then adding individual components and refining them as needed. To leverage top-down modeling, I started with a model of the handlebars and a model of my phone positioned how I would want my phone to be angled on the handlebars. Then, I projected the dimensions of the phone and the handlebars into my sketches for my custom components, ensuring that they’d fit together and work seamlessly.


# About the Design

![gif of rotation](/assets/img/bike phone mount.gif)
A key requirement of this assignment was the phone mount’s ability to rotate and snap into horizontal and vertical positions. For this, I designed an inner circle and an outer circle that it could rotate smoothly inside. The inner piece has a cavity for a compressional spring and a ball bearing, and the outer circle has rounded encaves matching the radius of the ball bearing. I balanced the length and flexibilty of the spring, diameter of the ball bearing, and sizes of the cavities so that the model can rotate easily by hand, but clicks securely into each of the four orientations.
It works awesomely – super smooth rotation between satisfying clicks for each orientation.



![detent mechnism](/assets/img/detent.png)
In this cross-sectional view of the detent mechanism, you can see the 7 mm ball bearing and 8x10 mm compressional spring that allow the phone to snap into vertical and horizontal orientations.
For this project, I used FFF 3D printing on Voron printers with a 0.6 mm nozzle.
For the phone holder part, I used TPU so I can easily pop my phone in and out of the phone mount. It fits snuggly so my phone will be secure even on a bumpy trail. For the clamp, I used ABS because I needed a rigid material with slight flexibility (strong, but not brittle) that could have heat-set inserts put in it and I used a TPU inlay for grip on the handlebars. I did the inside of the rotation mechanism in PLA because it needed to rotate smoothly and didn’t need to be flexible and my PLA prints usually have better print quality and are smoother than ABS parts I print.

In the model, the flexible components are white, and the rigid parts are red. 

# CAD Model

<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH90d2dQT28d5b602811b2d6ba3974e2de1a?mode=embed" width="800" height="600" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>
{% include gallery caption="Dimensioned Drawings for Custom 3D Printed Parts." %}


To account for the expansion of the filiment and possible dimensional inaccuracy, I added 0.5 mm of clearance in between the inner and outer components of the rotation mechanism. This worked well and the pieces rotate smoothly without the inner part jiggling around. I also increased the diameter of the spring cavity by 0.2 mm to ensure that the spring could fit inside. 


## Assembly and Use
To assemble the device, I used M3 x 5 mm bolts to attach the top part of the clamp to the inner part of the rotational mechanism, sandwiching the lip on the outer rotational component and holding all the pieces together. I slid the grippy TPU inlay into place on the clamp. The top and bottom parts of the clamp are connected by four M3 x 12 mm bolts which are tightened appropriately by the user to secure the mount onto the handlebars.

# Custom 3D Printed Parts

| **Item**             |
|----------------------|
| Motor Mounting Plate |
| Carriage             |
| Enclosure            |
| Lid for enclosure    |
| End support          |
| Syringe support      |

# Off the Shelf Parts

| **Item**                              | **Quantity** |
|---------------------------------------|--------------|
| M5x8mm bolt                           | 6            |
| M3x6mm bolt                           | 14           |
| M5 Tee nut                            | 4            |
| 10mm LED                              | 1            |
| V-slot 20x40x350mm aluminum extrusion | 1            |
| 10mm button switch                    | 3            |
| 8mmx200mm linear rod                  | 1            |
| 8mm lock collar                       | 2            |
| TR8 8x250mm lead screw                | 1            |
| limit switch                          | 1            |
| NEMA 17 Stepper Motor                 | 1            |
| 8mm flexible coupler                  | 1            |
| Arduino                               | 1            |
| TR8x8mm nut                           | 1            |
