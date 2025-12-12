
---
title: "Generative Design Truck"
excerpt: "Mount your phone to your bike - and rotate it!"
header:
  image: /assets/img/bikemountrender.png
  teaser: /assets/img/bikemountrender.png
gallery:
  - url: /assets/img/phoneholder.png
    image_path: assets/img/phoneholder.png
    alt: "phone holder"
  - url: assets/img/inside.png
    image_path: assets/img/inside.png
    alt: "inside"
  - url: /assets/img/clamptop.png
    image_path: /assets/img/clamptop.png
    alt: "top of clamp"
  - url: /assets/img/clampbottom.png
    image_path: /assets/img/clampbottom.png
    alt: "bottom of clamp"




---

I designed and filament 3D printed a rotating phone holder for a bike using top-down modeling. 

![irl image](/assets/img/phonemountirl1.png)

### Top-Down Modeling

Top-down modeling is an approach in design where you start with the overall concept or higher-level features of a product and then add individual components and refine them as needed. To leverage top-down modeling, I started with a model of the handlebars and a model of my phone positioned how I would want my phone to be angled on the handlebars. Then, I projected the dimensions of the phone and the handlebars into my sketches for my custom components, ensuring that they’d fit together and work seamlessly.



# About the Design

![gif of rotation](/assets/img/bike phone mount.gif)

A key requirement of this assignment was the phone mount’s ability to rotate and snap into horizontal and vertical positions. For this, I designed an inner circle and an outer circle so that it could rotate smoothly inside. The inner piece has a cavity for a compressional spring and a ball bearing, and the outer circle has rounded encaves matching the radius of the ball bearing. I balanced the length and flexibility of the spring, diameter of the ball bearing, and sizes of the cavities so that the model can rotate easily by hand, but clicks securely into each of the four orientations.

To account for possible warping and dimensional inaccuracy, I added 0.5 mm of clearance in between the inner and outer components of the rotation mechanism. This worked well and the pieces rotate smoothly without the inner part jiggling around. I also increased the diameter of the spring cavity by 0.2 mm to ensure that the spring could fit inside. It works awesomely – super smooth rotation between satisfying clicks for each orientation.


![detent mechnism](/assets/img/detent.png)
In this cross-sectional view of the detent mechanism, you can see the ball bearing and compressional spring that allow the phone to snap into vertical and horizontal orientations.

For this project, I used FFF 3D printing on Voron 300 printers with a 0.6 mm nozzle.
For the phone holder part, I used TPU so I can easily pop my phone in and out of the phone mount. It fits snuggly so my phone will be secure even on a bumpy trail. For the clamp, I used ABS because I needed a rigid material with slight flexibility (strong, but not brittle) that could have heat-set inserts put in it and I used a TPU inlay for grip on the handlebars. I did the inside of the rotation mechanism in PLA because it needed to rotate smoothly and didn’t need to be flexible and my PLA prints usually have better print quality and are smoother than ABS parts I print.


In the model below, the flexible components are white, and the rigid parts are red. 

# CAD Model

<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH90d2dQT28d5b602811b2d6ba3974e2de1a?mode=embed" width="800" height="600" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

### Custom 3D Printed Parts

{% include gallery caption="Fusion 360 renderings of top-down components. " %}



## Assembly and Use

To assemble the device, I started by pushing the ball bearing and spring down in the inside of the rotational component and fitting it into the outer circle.

I used M3 x 5 mm bolts to attach the top part of the clamp to the inner part of the rotational mechanism, sandwiching the lip on the outer rotational component and holding all the pieces together. 

The grippy TPU inlay slides into place on the clamp. The top and bottom parts of the clamp are connected by four M3 x 12 mm bolts which are tightened appropriately by the user to secure the mount onto the handlebars. Finally, I pop my phone into the flexible phone holder part, and it's ready to use.

| **Off the Shelf Parts**      | **Quantity** |
|------------------------------|--------------|
| M5x12mm bolt                 | 4            |
| M3x5mm bolt                  | 2            |
| M3 Heat-set insert           | 6            |
| 8x10mm compressional spring  | 1            |
| 7mm ball bearing             | 1            |
