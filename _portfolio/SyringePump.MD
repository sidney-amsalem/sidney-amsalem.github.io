---
title: "Syringe Pump"
excerpt: "An accurate, cost-effective, programmable DIY pump capable of various flow rates."
header:
  image: /assets/img/syringe-pump-cad.png
  teaser: /assets/img/syringe-pump-cad.png
gallery:
  # - image_path: assets/img/syringe-pump.jpg
  # - image_path: assets/img/Slide-2.png
  # - image_path: assets/img/Slide-4.png
   
---

The syringe pump is a cost-effective solution designed to provide precise fluid dispensing in various medical and laboratory applications. This programmable pump is compatible with multiple syringe sizes, allowing for easy adaptation without the need for tools or manual adjustments. Built with a focus on  user-friendliness, the pump features an intuitive interface with an on/off button and LED status indicators. The robust design includes an aluminum rail for the pump assembly and a protective enclosure for the electronics, ensuring durability and safety during operation.

# Features

* **Accurate and Programmable Flow Rate**: The syringe pump is designed to dispense liquids at a precise flow rate, adjustable via an Arduino program, making it suitable for medical situations requiring exact fluid control.
* **Versatile Syringe Compatibility**: Easily exchangeable with different syringe diameters without the need for tools, accommodating various sizes of syringes securely.
* **Robust Design**: The pump assembly is mounted on an aluminum rail, with electronics housed in a protective enclosure to shield against water exposure.
* **User-Friendly Interface**: The pump features an intuitive on/off button with an LED status indicator, making it simple to operate.
* **Built-in Fail Safe**: The pump automatically stops when the plunger reaches its limit.

# CAD Model

Explore the interactive Fusion 360 model of the Syringe Pump assembly below:
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a420c83ffe648ca368?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

# Operation Instructions

1. **Prepare the Syringe**: Insert the syringe barrel into the designated slot on the pump assembly. Ensure it is securely positioned with the flange fitting snugly into the support.
2. **Position the Plunger**: Manually turn the lead screw to move the carriage until the plunger fits into the carriage cutout.
3. **Power On**: Connect the power supply, and ensure the LED is yellow, indicating readiness.
4. **Start Dispensing**: Press the on button to begin dispensing. The LED will turn green, indicating that the pump is operating.
5. **Automatic Stop**: Once the syringe is empty, the limit switch will stop the motor, and the LED will turn red, signaling the completion of the process.
6. **Turn Off**: After dispensing, press the on button again to turn off the pump, unplug it, and remove the syringe.

# Off-the-Shelf Parts

| Part Name               | Description                            | Quantity |
|-------------------------|----------------------------------------|----------|
| NEMA 17 Stepper Motor   | Motor for driving the lead screw       | 1        |
| 2040 Aluminum Extrusion | 1-foot long extrusion for the base     | 1        |
| Lead Screw (8mm Pitch)  | 250mm lead screw for carriage motion   | 1        |
| Linear Rod (8mm)        | 8mm diameter rod for carriage stability| 1        |
| Power Supply (12V, 24V) | Powering the motor and Arduino         | 1        |

# 3D Printed Parts

| Part Name               | Description                                           | Quantity |
|-------------------------|-------------------------------------------------------|----------|
| Motor Mounting Plate    | Plate for securing the stepper motor                  | 1        |
| Carriage                | Moves along the lead screw to push the syringe plunger| 1        |
| Barrel Stabilizer (Front)| Supports the front of the syringe barrel              | 1        |
| Barrel Stabilizer (Back) | Holds the back of the syringe barrel securely         | 1        |
| Enclosure               | Protects electronics from exposure                    | 1        |
| Enclosure Lid           | Seals the enclosure, protecting internal components   | 1        |


<!-- {% include gallery caption="write caption here" %} -->
