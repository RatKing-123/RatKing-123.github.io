---
title: "Syringe Pump"
excerpt: "This syringe pump can dispense fluid at rates between 0.1 and 10.7‬‭ mL/min"
header:
  image: /assets/img/Syringe Pump Thumbnail.png
  teaser: /assets/img/Syringe Pump Thumbnail.png
gallery:
  - url: /assets/img/enclosure.png
    image_path: assets/img/enclosure.png
    alt: "placeholder image 1"
  - url: assets/img/lid.png
    image_path: assets/img/lid.png
    alt: "lid"
  - url: /assets/img/Syringe Pump Thumbnail.png
    image_path: /assets/img/Syringe Pump Thumbnail.png
    alt: "placeholder image 3"
---

 This syringe‬‭ pump‬‭ is powered‬‭ by‬‭ a‬‭ motor‬ coupled‬‭ to‬‭ a‬‭ lead‬‭ screw.‬‭ Key‬‭ design‬‭ considerations‬‭ include‬‭ adaptability‬‭ to‬‭ varying‬‭ syringe‬
‭ diameters‬‭ and‬‭ adjustable‬‭ flow‬‭ rates.‬‭ Additionally,‬‭ the‬‭ syringe‬‭ pump‬‭ incorporates‬‭ status‬‭ lights‬‭ for‬
‭ operational‬‭ feedback,‬‭ a‬‭ latching‬‭ button‬‭ for‬‭ control,‬‭ and‬‭ a‬‭ limit‬‭ switch‬‭ to‬‭ halt‬‭ motion‬‭ when‬‭ the‬
‭ plunger reaches its limit.

# CAD Model

<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a4e35ce33e8ec6886a?mode=embed" width="800" height="600" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>
{% include gallery caption="Dimensioned Drawings for Custom 3D Printed ." %}

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
