---
title: "Microfluidic Device"
excerpt: "This microfluidic device can sort particles by size."
header:
  image: /assets/img/ufluidDevice.png
  teaser: /assets/img/ufluidDevice.png
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
### Pinched Flow Fractionation (PFF)
Pinched flow fractionation (PFF) is a microfluidic separation technique that separates particles based on size. 
Two inlets, one with suspended particles and one with a buffer solution, enter a narrow pinched section. As they flow into the broad section, particles maintain their streamlined positions and small particles flow closer to the wall while large particles flow closer to the middle of the broad section. Outlets can then be strategically placed to collect the different sized particles.

A valuable application for PFF is sorting blood cells and platelets. Centrifugation or filtration can subject cells to mechanical stress and pressure differences that can damage delicate cells like platelets, but PFF uses smooth laminar flow, preserving cell viability. [Source: A comprehensive review of pinch flow fractionation in microfluidics](https://www.sciencedirect.com/science/article/pii/S0255270124004252)



# Design

For my design, I chose a symmetric approach. I placed my outlets at heights (y) based on the equation, $y=(pinched width - \frac{particle size}{2}\x\frac{Broad width}{Pinched width}$ where the width of the broad section was 44 mm, the pinched section was 1 mm, the large particles ranged from 425 to 500 µm, and the small particles ranged from 125 to 150 µm. The small channel height is at y = 41.03 and the large channel height y = 33.80 mm. The buffer channel was placed slightly above the midpoint of the large channel and the edge of the chip at y = 14.9 mm. All three channels were 0.75 mm wide.
I added a barrier to separate particles before they get to the outlets and prevent backflow at y = 37.65, halfway between the height for the minimum large particle size and the maximum small particle size, and another, halfway between the large particle and buffer channels at y = 23.4 mm.

To balance the flow, I increased the path lengths (increasing resistance) for the three outlets proportionally to how much fluid each should carry. I found that the small particle channel should take 14.4% of the fluid, the large particle channel should take 32.4%, and the buffer channel should take the remaining 53.2%. I scaled up this ratio as much as possible while following design constraints to maximize resistance differences on the chip. The path lengths were 110.1 mm for the small particles, 49.0 mm for the large particles, and 29.9 mm for the buffer channel. I used curved paths to mitigate bubble accumulation and add whimsy. 

If I were to iterate on this design, I would build a device to hold and support the flexible tubing to minimize differences in flow due to the changing positions of those tubes.

# CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH90d2dQT28d5b6028115d5d1c4bc6219274?mode=embed" width="800" height="600" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

# Instructions for Operation

‭1.‬‭ Copy this [Arduino code](https://github.com/RatKing-123/RatKing-123.github.io/blob/main/Ardiuno%20Code%20for%20Syringe%20Pump?h=1) into an Arduino sketch.‬

2.‬‭ Change the “volumetric_flow_rate” variable to the desired flow rate (in mL/min).‬

‭3.‬‭ Change the “total_volume” variable to the starting volume present in the syringe.‬

‭4.‬‭ Plug in the Arduino to the computer and upload the sketch.‬

5.‬‭ Unplug the Arduino from the computer and plug in the power chord from the pump.‬ The time to dispense should show on the LCD, and the LED should be yellow.‬

6.‬‭ Press the forward and backward buttons to adjust the plunger position if necessary.‬

‭7.‬‭ Press the start button to begin dispensing.‬

‭8.‬‭ Once‬‭ dispensing‬‭ is‬‭ complete‬‭ (LED‬‭ is‬‭ red),‬‭ press‬‭ the‬‭ start‬‭ button‬‭ again‬‭ to‬‭ move‬‭ back‬‭ into‬‭ manual control mode.‬

9.‬‭ Use the backward button to reset the pump to the desired position.‬

