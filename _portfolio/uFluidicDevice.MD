---
title: "Micro-Fluidic Device"
excerpt: "Cost-effective, 3D-printed device for efficient small-scale fluid mixing."
header:
  image: /assets/img/ufluidic-setup.jpg
  teaser: /assets/img/ufluidic-working.jpg
gallery:
  - image_path: assets/img/ufluidic-casted.jpg
  - image_path: assets/img/ufluidic-mold.jpg

   
---

# Introduction to Microfluidic Devices

Microfluidic devices are engineered systems designed to manipulate and process small volumes of fluid, typically in the range of nanoliters to microliters, through micro-scale channels. Microfluidic devices have numerous applications, including medical diagnostics, drug development, and chemical analysis. One important function of microfluidic devices is homogeneous mixing which is crucial in processes like drug formulation and chemical reactions to ensure uniform distribution of reagents.

These devices can be fabricated using  3D resin printing, which allows for creating precise molds at a significantly lower cost compared to traditional methods like stereolithography, saving thousands of dollars. The channels in microfluidic devices are often as small as 60 micrometers, about the width of a human hair. By working with such small volumes, microfluidics helps to reduce reagent and sample consumption, thereby making the testing process more cost-effective and efficient. For instance, using microfluidic devices to mix a small droplet of blood with reagents minimizes the use of expensive reagents.

Mixing in microfluidic devices presents challenges due to laminar flow at micro scales. In laminar flow, fluids move in parallel layers with minimal lateral mixing. To overcome the limitations of laminar flow, microfluidic devices employ specific channel geometries that generate chaotic advection—where individual fluid particles deviate from the straight laminar flow lines due to underlying microscale disturbances or structures in the flow.



### *Rationale Behind the Design*

#### **Channel Dimensions**

The channel dimensions were chosen to balance mixing efficiency with ease of fabrication. Although the resin printer used in this project has a minimum feature size of 85 micrometers, a channel width of 0.3 mm for the inlets and 0.6 mm for the main mixing channel was selected. This size ensures that the channels are large enough to facilitate mold casting with PDMS while also being small enough to enhance mixing through increased surface area for diffusion. Although smaller channels could further improve mixing, they present increased fabrication challenges and a higher risk of clogging.

#### **Zig-Zag Channel**

The zig-zag channel was included to induce chaotic advection and disrupt the orderly flow of the fluid. The zig-zag pattern forces the fluid to undergo repeated stretching and folding, which helps mix different layers of the fluid more effectively. This design is particularly useful for promoting mixing in laminar flow conditions where turbulence is absent.

#### **Split and Recombine Channel**

After the zig-zag section, the fluid passes through a split and recombine channel. This geometry works by dividing the fluid into multiple streams, increasing the interfacial contact area, and then recombining them. The process of splitting and recombining rearranges the fluid streams, which enhances diffusion-based mixing by shortening the distance molecules need to travel to diffuse across layers.

#### **Inclined Mixer Channel**

The inclined mixer channel further enhances mixing by creating complex flow paths. This channel includes a twisted geometry that forces the fluid to rotate and stretch, maximizing interaction between fluid layers. The design features a limiting hole of 0.09 mm², which helps control the flow rate and promotes chaotic mixing by adding restrictions that induce additional fluid deformation.

#### CAD Model

Explore the interactive Fusion 360 model of the Syringe Pump assembly below:
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a4d84411c215a0cf13?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>



### **Results**

We connected the microfluidic device to two syringe pumps, each with a 20 ml syringe that had an internal diameter of 18.7 mm. Considering the cross-sectional area of the inlet channels (0.3 mm x 0.6 mm), we began with a flow rate of 1.8 ml/min per syringe, resulting in a combined output of 3.6 ml/min. At this initial flow rate, the device demonstrated completely effective mixing, even before reaching the split and twisted channel sections. This effective mixing was attributed to the small channel size, which maximized the surface area and induced efficient mixing through friction between the fluid and channel walls.

Encouraged by these results, we increased the flow rate to the maximum output of the syringe pumps, approximately 3.11 ml/min per syringe. Despite the 76% increase in flow rate, which reduced the contribution of passive diffusion due to the higher fluid velocity, the device still achieved completely effective mixing, even before reaching the split and twisted channels. This demonstrates the importance of the small channel size in promoting efficient mixing across a wide range of flow rates.

### **From 3D Printed Mold to Final Device**

To fabricate the microfluidic device, follow these steps:

1. **Print and Cure the Mold**:

   - Print the mold using a high-resolution Form 3+/4 SLA printer. Ensure the design orientation prevents resin pooling in the channels.
   - Wash and Cure the mold:
     - Wash the mold in isopropyl alcohol using the FormWash system for 5 minutes. Then use a fresh IPA bath, with the mold placed in a basket and moved to help remove excess resin. Compressed air was also used to dislodge any remaining resin.
     - Let the mold dry upside down for 30 minutes to ensure complete removal of IPA, avoiding pooling in the channels.
     - Perform a 10-second surface cure in the FormCure. This shorter curing time prevents warping of the mold.

2. **Parylene Coating**:

   - Apply a parylene coating to the mold. This step is critical to prevent PDMS curing inhibition, which can be caused by photoinitiators leaching from the resin. Additionally, the parylene layer improves the biocompatibility of the mold, which is crucial for applications involving live cells.

3. **Cast PDMS**:

   - Mix SYLGARD™ 184 silicone elastomer (PDMS) at a 10:1 ratio of base to curing agent. Degas the mixture in a vacuum chamber to remove air bubbles.
   - Pour the PDMS over the mold and let it cure. Temperatures above 100°C will crack the clear resin, therefore the curing can be done at one of the following:
     - 23°C for 24 hours.
     - 65°C for 4 hours.
    - Once the PDMS has cured, carefully peel it off the mold. Bond the PDMS to a glass slide.

By following these steps, the 3D-printed mold can be used to create a functional microfluidic device designed for homogeneous mixing. Such devices are applicable in areas like biomedical diagnostics, chemical synthesis, and drug delivery. The design choices—ranging from channel dimensions to the inclusion of zig-zag, split-and-recombine, and inclined mixer geometries—were made to optimize mixing performance while maintaining ease of fabrication.

