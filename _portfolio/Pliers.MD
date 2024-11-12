---
title: "Multi-Material Pliers"
excerpt: "Multi-material pliers with flexible TPU spring"
header:
  image: /assets/img/plier-CAD.JPG
  teaser: /assets/img/plier-CAD.JPG
   
---

### Multi-Material Print-in-Place Needle Nose Pliers

In this project, I designed and printed multi-material print-in-place needle nose pliers. Print-in-place models work right after removal from the print bed, eliminating the need for post-processing or assembly.

<img src="/assets/img/plier-1.png" width="250"/>
<img src="/assets/img/plier-2.png" width="250"/>

#### Print-in-Place Parts
Print-in-place parts are designed with movable or flexible components that function immediately after printing. A popular feature in these designs is the use of joints, commonly seen in models with chains and hinges. These designs use small clearances (called negative space) to allow movement without separate assembly. Using flexible and rigid materials is popular with print-in-place parts. Rigid materials like PLA provide structure, while flexible materials like TPU enable elasticity and can be used as a spring or joint, allowing for natural movement. The automotive and aerospace industries use print-in-place parts to create lightweight components with integrated hinges or flexible joints, reducing the need for assembly and minimizing production times.

#### Design Process and Material Selection

<img src="/assets/img/plier-CAD.png" style="width: 400px"/>

**Material Choices and Assembly**: PLA was chosen for the plier body (handle and jaw). This is strong enough for the application, easy to print, and most importantly, rigid.  95A TPU was chosen for the center spring component because its flexibility allows for the plier’s spring-back effect. While the project can be printed on a multi-material printer, allowing for the pliers to be ready right after printing, two printers were used (one with PLA and the other with TPU). The parts were press fit together. This approach allowed me to test different variations of the spring and plier body independently of each other. The single extrusion printers were also faster (dual-extrusion printers are generally significantly slower) and more available (only 1 dual-extrusion printer was available in the lab).

**Dove Tail Joint**: TPU and PLA do not bond well with each other due to their differing mechanical properties (rigid vs. flexible). Interlocking dove tails were used to connect the TPU spring component with the PLA plier body. This allows for a connection without fasteners or adhesive.

**Design Iterations**: Early prototypes with round or flat-tipped jaws were ineffective at gripping small objects like resistors. Switching to a sharp-pointed design increased precision and improved the pliers' ability to grab resistors by both body and wire. Other design details included fillets to reduce sharp edges and a handle cutout to save material and reduce print time.

**TPU Spring**: Fusion 360's pattern-on-path tool simplifies designs with repetitive sketches and features. Only a single dovetail needed to be created, as the remaining dove tails can be patterned along the edge of the spring component (and plier handles). The TPU spring component was designed with a cross pattern, creating resistance when the pliers are compressed and springing back to when released. The spring’s cross pattern was created through SuperSlicer's infill pattern and density settings. By selecting monotonic/rectilinear infill patterns with densities of 10-13%, setting top and bottom layers shell layers to 0, and setting perimeters count between 3-5, I printed a range of spring components with varying flexibilities. For my pliers with a thickness of 5.5mm, a spring component with 13% fill density, monotonic fill pattern, and 5 perimeters gave the pliers a firm but flexible feel.

<img src="/assets/img/plier-spring.png" style="width: 300px">

#### Plier Specifications

| Specification     | Measurement |
|-------------------|-------------|
| Length            | 143mm       |
| Jaw Length        | 32mm        |
| Jaw Capacity      | 7.2mm       |
| Handle Length     | 72mm        |
| Thickness         | 5.5mm       |

<img src="/assets/img/pliers-working.GIF" style="width: 400px">


