---
title: "Microfluidic Device"
excerpt: "This microfluidic device can sort particles by size."
header:
  image: /assets/img/ufluidDevice.png
  teaser: /assets/img/microfluidrender.png
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

![PFF Diagram](/assets/img/PFF.png)
[*Source: Pinched Flow Fractionation*](https://pubs.acs.org/doi/10.1021/ac049863r)

A valuable application for PFF is sorting blood cells and platelets. Centrifugation or filtration can subject cells to mechanical stress and pressure differences that can damage delicate cells like platelets, but PFF uses smooth laminar flow, preserving cell viability. [*Source: A comprehensive review of pinch flow fractionation in microfluidics*](https://www.sciencedirect.com/science/article/pii/S0255270124004252)

<script type="text/javascript"
  id="MathJax-script"
  async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

# Design

For my design, I chose a symmetric approach. I placed my outlets at heights (y) based on the equation,
 ![Equation](https://latex.codecogs.com/svg.latex?Y_0=\left(w_p-\frac{D}{2}\right)\frac{w_b}{w_p})  , where Wp = width of the pinched section, Wb = width of the broad section, D = particle diameter. 

The width of the broad section was 44 mm, the pinched section was 1 mm, the large particles ranged from 425 to 500 µm, and the small particles ranged from 125 to 150 µm. The small channel height is at y = 41.03 and the large channel height y = 33.80 mm. The buffer channel was placed slightly above the midpoint of the large channel and the edge of the chip at y = 14.9 mm. All three channels were 0.75 mm wide.

I added a pointed barrier to separate particles before they get to the outlets and prevent backflow at y = 37.65, halfway between the height for the minimum large particle size and the maximum small particle size, and another, halfway between the large particle and buffer channels at y = 23.4 mm.

![Sketch](/assets/img/sketch.png)

To balance the flow, I increased the path lengths (increasing resistance) for the three outlets proportionally to how much fluid each should carry. I found that the small particle channel should take 14.4% of the fluid, the large particle channel should take 32.4%, and the buffer channel should take the remaining 53.2%. 

I scaled up this ratio as much as possible while following design constraints to maximize resistance differences on the chip. The path lengths were 110.1 mm for the small particles, 49.0 mm for the large particles, and 29.9 mm for the buffer channel. I used curved paths to mitigate bubble accumulation and add whimsy. 


# CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH90d2dQT28d5b6028115d5d1c4bc6219274?mode=embed" width="800" height="600" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>
*Fusion360 model of the mold for my device.*



# To Create the Device:

1. Resin print a mold for the device.
2. Post processing: Wash with isopropyl alcohol to remove all uncured resin and post-cure with UV for structural integrity.
3. Coat the mold in a thin layer of parylene to prevent resin leaching into the PDMS and interfering with cross-linking.
4. Cast the device in PDMS (polydimethylsiloxane) using the mold. After setting, carefully demold the device.
![mold and PDMS device side by side](/assets/img/moldAndPDMS.png)
5. Plasma bond the PDMS device to a glass slide. This makes it so the channels are watertight (pictured below)
![plasma bonding process](/assets/img/Plasma-Treating-Image.jpg)




# Discussion

Resin printing offers smooth, optically clear channels, high resolution, and complex 3D geometries, making it particularly advantageous for microfluidic devices with carefully defined pinched and broad zones– features that demand tight dimensional precision and smooth surfaces.

#### Real-World Application!
Given the particle size range my device is equiped to handle, a real-world application for it would be separating fine (125-150 µm) and coarse (425-500 µm) sand grains for sediment monitoring in a river or stream. Understanding the grain-size distribution of sediments in rivers and streams is important for sediment transport modeling, pollutant tracking, and habitat mapping, which are all indicators of overall stream health. 

Traditionally, these data come from manual sieving or laser diffraction, both of which require batch sampling and lab analysis. PFF could offer a way to make this process field-deployable, saving time and money.


#### Scaling up
To handle a wider range of particle sizes, my design could be scaled up and use multiple stages of pinched and broad sections. I would first separate out the largest particles then narrow down to a finer scale to separate out the smallest particles. It would be similar to multi-stage sieving, but happen all on one chip. When separating the smallest particles, the broad section could be widened to increase the distance between the particle streams, allowing for separation even at a very fine scale. 

#### Particle Size Limits
PFF separates particles based on how their size causes them to occupy different streamlines in a pinched microchannel. For separation to work, the particle diameter must be large enough that its centerline position shifts measurably relative to smaller particles as it passes through the pinched region and also be large compared to fabrication roughness or surface irregularities. If particles are too small, they follow nearly the same streamline as the fluid, experience [Brownian motion](https://en.wikipedia.org/wiki/Brownian_motion), and are dominated by diffusion rather than geometry-driven displacement.

#### Testing and Future Solutions
During the testing process (setup pictured below) the device did not successfully sort particles due to issues with the density of the suspension and back pressure from slight movements of the flexible tubes. If I were to iterate on this design, I would build a device to hold and support the flexible tubing to minimize variability in resistance due to the changing positions of those tubes.
![testing setup](/assets/img/testingsetup.png)






