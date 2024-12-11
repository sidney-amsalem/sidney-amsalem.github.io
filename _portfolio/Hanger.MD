---
title: "Motorized Longboard Hanger"
excerpt: "Created using a Generative Design approach"
header:
  image: /assets/img/hanger-8.PNG
  teaser: /assets/img/hanger-8.PNG
   
---
# Introduction to Generative Design

Generative design is a design methodology that uses algorithms to create designs based on parameters or constraints. The process involves inputting certain design goals, constraints, and loads, and then using software to automatically generate design options. By using generative design, engineers can create components that are stronger and lighter than components created with a traditional design pipeline. 

NASA’s Jet Propulsion Lab used generative design to create a lightweight, optimized design for the Europa lander, reducing mass and maintaining strength. Aerospace assemblies are often composed of multiple parts, but generative design allows the merging of these components into a single structure. The lander’s legs are traditionally made of many smaller pieces but were generated as a single part. This simplifies manufacturing (with the caveat of requiring powder bed fusion) and also enhances reliability by reducing the number of components and potential points of failure.

I am using Fusion 360’s generative design feature to design a motorized longboard hanger. By using generative tools, this longboard hanger will balance strength and reduced weight, much like NASA’s approach to the Europa lander. Generative design will be useful to create a design that will consider additional forces from the motor, like torque and belt tension. This approach will result in a design that can withstand both the rider's weight and the stresses of the motor.

## The Importance of Applying the Proper Load Cases

I decided to place two separate constraints on the longboard hanger, as it interacts with the baseplate through the pivot point and kingpin through-hole. I applied a pin constraint at these locations because the hanger’s motion around the pivot point and kingpin through-hole is most similar to rotation during turning. The pivot point constraint allows the hanger to rotate and the kingpin constraint simulates how the load is transferred between the hanger and baseplate. These two constraints are necessary for the simulation to reflect realistic loading scenarios.

I placed a total of eight unique loads on the model to account for the variety of forces that a longboard truck can experience. These loads are:

- **Rider weight on the axle:** A 2000N bearing load was applied to the inner cylinder of the hanger that accepts the axle. This simulates forces significantly greater than the rider’s weight, considering impacts from bumps and small jumps.
- **Medial force from the wheel during turning:** Estimated at 300N on each side of the hanger for extreme turning cases, equating to roughly 67 lbs of force.
- **Axle stress from turning:** Moments of 15 Nm (clockwise and counterclockwise) were applied along the axle hole to represent bending stresses from lateral forces during turning.
- **Force on the kingpin through-hole:** Simulated with three bearing loads on the inner cylindrical surface: one vertically upward (1200N) and two lateral (400N each).
- **Pivot point forces:** A downward vertical force of 1000N and two 600N forces angled 55 degrees from vertical simulated turning forces at the pivot point.
- **Motor weight:** A 15N downward remote force was applied to the motor mount to account for the motor’s weight and additional impact forces from the road.
- **Motor torque:** An 8 Nm counterclockwise moment was applied to the motor mount to simulate the motor’s torque.
- **Belt tension:** A 400N remote force was applied to the motor mount’s pulley center, pointing to the large pulley on the wheel, to simulate static and dynamic belt tension. After printing the model, it struck me that an equal and opposite belt tension force should have been applied from the large pulley back to the motor pulley.

The load calculations described above were generated with the help of ChatGPT. I have reviewed and adjusted these values based on intuition and common sense. Most loads above are over-compensated to account for any shocks and large rises in forces when the longboard is ridden over bumps and in extreme turning scenarios.

## Comparison of Nylon and Aluminum Generative Design Outcomes

<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a47f452b9c783afa5b?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>
ALSi10Mg Truck Hanger

<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a42fd469a036d0d453?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>
Nylon 12 Truck Hanger

The following settings were used to generate the outcomes:

- Minimum safety factor: 1.5
- Design criteria: Minimize mass
- Manufacturing method: Unrestricted
- Materials: Nylon 12 and AlSi10Mg

Two outcomes, one made of Nylon 12 and one of Aluminum (AlSi10Mg) were created. Below is a table with statistics of their properties. To better understand the differences between the two, it is important to know the following terms in relation to these designs:

- **Max von Mises Stress:** Indicates the maximum combined stress at a point, helping determine whether the material will yield under a given load.
- **Max displacement:** Represents the largest distance any part of the design moves under the applied loads, affecting deformation and usability.
- **Safety factor:** Indicates the margin of safety before failure, with higher values representing a more reliable design.

| Property                        | Aluminum (AlSi10Mg) | Nylon 12     |
|----------------------------------|---------------------|--------------|
| Volume (mm³)                     | 70,425              | 404,878      |
| Mass (kg)                        | 0.188               | 0.411        |
| Max von Mises Stress (MPa)       | 79.848              | 30.667       |
| Max displacement (mm)            | 0.797               | 20.958       |
| Safety Factor (Min)              | 3.006               | 1.5          |

Visually, these two outcomes are extremely different due to the distinct mechanical properties of the materials. Nylon is more flexible and requires a bulkier design to handle the applied forces, while aluminum is stiffer and can achieve a minimalistic design due to its higher strength.

The aluminum design is significantly stronger with a maximum von Mises stress of 79.848 MPa, compared to nylon’s 30.667 MPa. It also exhibits better stiffness with a maximum displacement of 0.797 mm, compared to nylon’s 20.958 mm. Additionally, aluminum is significantly lighter, weighing less than half of the nylon design, despite using approximately 5.7 times less volume of material. Both designs meet the safety factor limit of 1.5, but aluminum’s higher minimum safety factor of 3.006 offers a greater margin for stresses encountered during use, such as bumps, jumps, and extreme turns, making it the superior choice for a skateboard hanger.

## Critique of Generative Design

Generative design is great in creating optimal geometries that are often lighter and stronger than traditional designs. However, its applications are limited by the following challenges:

### Manufacturing Complexity and Costs:
The intricate geometries often produced by generative design most likely require advanced additive manufacturing methods, such as powder bed fusion. These methods are expensive and time-intensive, limiting their use for consumer-grade products and applications.

### Research and Development Costs:
The design efforts required to implement generative design can be substantial. Spending the time and effort on generative design may not be worth it for applications that don’t necessarily require the most optimal geometry.

In my opinion, generative design is best in low-volume and technically demanding applications. Producing large volumes of generative designed parts is impractical due to manufacturing constraints and costs.

Generative design does well in areas where performance optimization is critical and cost is not a limiting factor. Aerospace is a great example, where lightweight, high-strength parts justify the investment. 

In space exploration, weight reduction is important to save on launch costs. For instance, the current cost for a payload on the 2018 SpaceX Falcon Heavy rocket is roughly $1500 per kilogram. This gives a good perspective on how important weight savings are in the aerospace industry. SpaceX is working towards a $10 per kilogram cost with the reusable Super Heavy Starship, and generative design can be a huge help towards that goal. Cost savings due to reduced weight would justify the investment in generative design to produce lightweight parts. 

## Conclusion and Gallery

Generative design is a powerful tool in the right context. However, for most industrial and consumer-based applications, it remains constrained by manufacturing and economic limitations, making traditional design a better choice.

## Model Renderings

<span>
    <img src="/assets/img/hanger-7.PNG" width="250"/>
    <img src="/assets/img/hanger-8.PNG" width="250"/>
</span>

## Printed Model

Real life images of the ALSi10Mg model pSLS printed and attached to the longboard deck

<span>
    <img src="/assets/img/hanger-1.JPG" width="250"/>
    <img src="/assets/img/hanger-2.JPG" width="250"/>
</span>
<span>
    <img src="/assets/img/hanger-3.JPG" width="250"/>
    <img src="/assets/img/hanger-4.JPG" width="250"/>
</span>
<span>
    <img src="/assets/img/hanger-5.JPG" width="250"/>
    <img src="/assets/img/hanger-6.JPG" width="250"/>
</span>


