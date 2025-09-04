---
title: "Syringe Pump"
excerpt: "This syringe pump can dispense fluid at rates between 0.1 and 10.7‬‭ mL/min"
header:
  image: /assets/img/Syringe Pump Thumbnail.png
  teaser: /assets/img/Syringe Pump Thumbnail.png
gallery:
  - url: /assets/img/Syringe Pump Thumbnail.png
    image_path: /assets/img/Syringe Pump Thumbnail.png
    alt: "placeholder image 1"
  - url: /assets/img/Cyber-Scooter-2.jpg
    image_path: /assets/img/Syringe Pump Thumbnail.png

    alt: "placeholder image 2"
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
{% include gallery caption="This is a sample gallery to go along with this case study." %}

# Instructions for Operation

‭1.‬‭ Copy this [Arduino code](https://github.com/RatKing-123/RatKing-123.github.io/blob/main/Ardiuno%20Code%20for%20Syringe%20Pump?h=1) into an Arduino sketch.‬
2.‬‭ Change the “volumetric_flow_rate” variable to the desired flow rate (in mL/min).‬
‭3.‬‭ Change the “total_volume” variable to the starting volume present in the syringe.‬
‭4.‬‭ Plug in the Arduino to the computer and upload the sketch.‬
5.‬‭ Unplug the Arduino from the computer and plug in the power chord from the pump.‬
‭ a.‬‭ The time to dispense should show on the LCD, and the LED should be yellow.‬
6.‬‭ Press the forward and backward buttons to adjust the plunger position if necessary.‬
‭7.‬‭ Press the start button to begin dispensing.‬
‭8.‬‭ Once‬‭ dispensing‬‭ is‬‭ complete‬‭ (LED‬‭ is‬‭ red),‬‭ press‬‭ the‬‭ start‬‭ button‬‭ again‬‭ to‬‭ move‬‭ back‬‭ into‬‭ manual control mode.‬
9.‬‭ Use the backward button to reset the pump to the desired position.‬

# Off the Shelf and 3D Printed Parts

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |
‭
