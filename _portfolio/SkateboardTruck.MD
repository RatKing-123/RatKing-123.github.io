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

First, I placed the fixed structural constraint where the bushings hold the center of the hangar, because it shouldn’t move. 

Then, I put a 150N force on each side (opposite directions) to simulate turning. I used a 2lb downward force to simulate the weight of the motor. 19.2 N m moment to account for torque of the motor. 


## Nylon vs. Aluminum

For this assignment, we generated outcomes for two separate materials: Nylon 12 and ALSi10Mg.

![side by side](/assets/img/sidebysiderender.png)

Since the Nylon has much less strength than the Aluminum, the generative design program determined that the Nylon outcome needed significantly more material.

<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH90d2dQT28d5b60281189fed872550a8ee0?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH90d2dQT28d5b602811ef257069bd9d289e?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>


![real life image of assembly](/assets/img/truckirl.png)
![video of it working](/assets/img/truck (1).gif)
