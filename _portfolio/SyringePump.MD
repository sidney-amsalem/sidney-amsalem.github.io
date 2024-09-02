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

# Purpose and Features

The Syringe Pump is a cost-effective, accurate, and programmable device designed for precise fluid dispensing in medical and laboratory settings. It offers adaptability to various syringe sizes without the need for tools, making it easy to switch between different applications. The design features an intuitive interface with an on/off button and LED status indicators for user-friendly operation. Built on a durable aluminum rail with a protective enclosure for the electronics, the pump is designed to withstand rigorous use while ensuring safety and reliability.

# Off-the-Shelf Parts

| Part Name                | Description                                            | Quantity |
|--------------------------|--------------------------------------------------------|----------|
| Arduino                  | Microcontroller for controlling the motor and sensors  | 1        |
| Power Supply             | Powers the motor and Arduino                           | 1        |
| Breadboard               | For the electrical circuit                             | 1        |
| On/Off Switch            | Controls the power to the motor                        | 1        |
| M3 Screw                 | Fasteners for various components                       | 14       |
| Aluminum Rail (V-Slot)   | 1-foot long extrusion for the base                     | 1        |
| M5x8mm Bolt              | Secures components to the aluminum rail                | 6        |
| M5 Tree Nut              | Inserts into the aluminum rail for mounting components | 10       |
| NEMA 17 Stepper Motor    | Motor for driving the lead screw                       | 1        |
| M3x10mm Bolt             | Secures the stepper motor                              | 4        |
| M3x8 Thread Forming Screw| Secures the electronics enclosure                      | 4        |
| Linear Bearing           | Guides the carriage along the linear rod               | 1        |
| Nut TR8x8-4              | Nut for the lead screw                                 | 1        |
| Linear Rod Lock Collar   | Holds the linear rod in place                          | 2        |
| Linear Rod 8mmx200mm     | Provides stability for the carriage                    | 1        |
| Lead Screw TR8x8x250mm   | Drives the carriage for syringe dispensing             | 1        |
| Flexible Coupler         | Connects the motor to the lead screw                   | 1        |
| Flanged Ball Bearing     | Provides smooth rotation for the lead screw            | 2        |



# 3D Printed Parts

| Part Name               | Description                                           | Quantity |
|-------------------------|-------------------------------------------------------|----------|
| Motor Mounting Plate    | Plate for securing the stepper motor                  | 1        |
| Carriage                | Moves along the lead screw to push the syringe plunger| 1        |
| Barrel Stabilizer (Front)| Supports the front of the syringe barrel              | 1        |
| Barrel Stabilizer (Back) | Holds the back of the syringe barrel securely         | 1        |
| Enclosure               | Protects electronics from exposure                    | 1        |
| Enclosure Lid           | Seals the enclosure, protecting internal components   | 1        |

# Arduino Code

The Arduino code for controlling the syringe pump is available on [GitHub](https://github.com/sidney-amsalem/syringe-pump-arduino-code). This code manages the motor speed based on the syringe diameter and flow rate, controls the LED status indicators, and ensures safe operation with the limit switch.

<!-- {% include gallery caption="write caption here" %} -->
