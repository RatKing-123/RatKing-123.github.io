---
title: "Generative Design Skateboard Truck"
excerpt: "Lightweighted truck hanger with an integrated motor mount "
header:
  image: /assets/img/truckrender.png
  teaser: /assets/img/truckrender.png
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

I created a topology optimized skateboard truck using generative design and powder printing. The objective was to to create a lightweight truck hanger with an integrated motor mount for a brushless DC motor.
![real life image of assembly](/assets/img/truckirl.png)

## Generative Design & Powder Bed Fusion

This pairing is complementary because:
- Generative design/topology optimization can propose highly efficient geometries (thin ribs, branching struts, lattices), minimizing mass while meeting stiffness/strength constraints.
- Metal powder bed fusion is one of the few production-capable processes that can actually manufacture those complex internal/organic geometries without tooling, and with fine feature control—so the “weird” shapes that are optimal on a solver aren’t automatically disqualified by manufacturability.

This combo shines in aerospace and automotive when you want some mix of lightweighting, part consolidation, high performance per weight, and shorter iteration cycles.

### [Divergent BrakeNode](https://www.divergent3d.com/applications/automotive)
This example features an integrated brake caliper and suspension upright, enabling improved braking performance and up to a 40% reduction in unsprung mass versus a conventional caliper & upright package. 

![Divergent BrakeNode](/assets/img/brakenode.png)
*Image Source: [Divergent](https://www.divergent3d.com/applications/automotive)*

Although the “final form” involves multiple printed nodes + tubes/rods, the design philosophy is still assembly simplification. With the BrakeNode, Divergent reduces tooling and consolidates structure/function into fewer, more optimized elements.

## Importance of Load Cases

Generative design only optimizes where you tell it to. It redistributes material to satisfy applied forces and moments, boundary conditions, and constraints the user inputs. So, if a load case is missing, the model won’t have material generated to account for that scenario.




For my skateboard truck, I knew I should consider: 
- Weight of the rider
- Shear force experienced by the trucks (turning, tricks, etc.)
- Motor torque
- Motor weight
- Belt tension

First, I placed the fixed structural constraint to the kingpin through-hole in the center of the hanger, because it shouldn’t move. 

Then, I put a 150N force on each side (opposite directions) to simulate turning. I used a 2lb downward force to simulate the weight of the motor. 19.2 N m moment to account for torque of the motor. 

To improve this process, I could build multiple load cases to handle a set of more specific scenarios like carving at speed, braking hard, or dropping off a curb. Then my model would be able to survive all of them. Simulating all of these actions would require more complex calculations and accurate placement of forces than the ones I used, but it could be done to make a very high performance skateboard. Designs could also go through an iterative process where they are printed, tested, forces measured, and redesigned accordingly.  

## Nylon vs. Aluminum

For this assignment, we generated outcomes for two separate materials: Nylon 12 and ALSi10Mg.

![side by side](/assets/img/sidebysiderender.png)

Since the Nylon has much less strength than the Aluminum, the generative design program determined that the Nylon outcome needed significantly more material.

<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH90d2dQT28d5b602811ef257069bd9d289e?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

The Nylon 12 model above has a mass of 0.543 kg, and has a volume 5.5x greater than the ALSi10Mg model shown below.

<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH90d2dQT28d5b60281189fed872550a8ee0?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

The Aluminum outcome has a mass of 0.26 kg, and is so lightweight and sleek!

### Final Assembly
The optimized aluminum outcome was powder printed and assembled. This step showed me how important it was to correctly assign obstacle geometries and clearances to ensure proper fit between parts.


Here's a video of the full assembly working!
![video of it working](/assets/img/truck (1).gif)

### Final Thoughts on Generative Design

I think generative design can be useful, but is easy to oversell. To be successful, generative design has to be partnered with strong engineering judgement rather than used as a replacement. 

The success of generative design is completely dependent on how accurately forces are calculated and placed, so it’s still important to have an accurate understanding of conditions. Also, the generated designs should always be checked by a person for errors. 

For this project, it took significantly longer to determine forces, assign preserved and obstacle geometries, and wait for Fusion360 to generate outcomes that it would’ve to just model my own truck. I did really enjoy getting to powder print the organic geometries created because the part came out looking so much nicer than a filament printed rendition would.

Lightweighting this skateboard truck made a relatively small impact, but for other applications, the impact could be quite meaningful. In areas like aerospace engineering and robotics where the forces are known and every little bit of weight can make a difference, generative design could be very useful.

