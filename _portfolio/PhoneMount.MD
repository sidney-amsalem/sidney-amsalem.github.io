---
title: "Bike Phone Mount"
excerpt: "Built using a Top-Down Modeling Approach"
header:
  image: # assets/img/mount-1.png
  teaser: assets/img/mount-1.png
gallery: 
  - image_path: assets/img/mount-1.png
  - image_path: assets/img/mount-2.png
  - image_path: assets/img/mount-3.png
  - image_path: assets/img/mount-4.png
  - image_path: assets/img/mount-5.png
  - image_path: assets/img/mount-6.png
   
---

## Project Overview

This bike phone mount was designed to securely grip a 23 mm handlebar and an iPhone 12 Pro with an integrated TPU case, with a non-invasive installation. The design allows users to attach the mount using only an Allen key, avoiding damage to the handlebar such as drilling or set screws. The mount's rotating mechanism enables the phone to lock into vertical or horizontal positions, which can be changed mid-ride without tools. This was achieved using a male-female locking mechanism, tensioned by a spring for a satisfying snap.

## Top-Down Modeling

Top-down modeling is a design approach where components are created in relation to each other within the context of an assembly. This ensures precise fit, reduces errors in part alignment, and streamlines the design process by allowing components to be directly modeled based on their relationships within the assembly. For instance, the male-female rotating mechanism was modeled together, using projections to guarantee a proper fit without measuring and using dimensions. Similarly, the phone case's bolt holes were aligned with the mount by projecting geometries from the mount onto the phone case. An iPhone 12 Pro model from GrabCAD streamlined the design process, allowing for accurate projections and dimensioning.

## Material Choice

- **TPU (FFF)**: Used for the phone case and bottom handlebar mount. Its flexible properties allows parts to securely grip both the phone and handlebar without causing damage.
- **Resin (VPP)**: Used for the main housing due to its complex geometry, making it ideal for detailed prints with minimal/easy-to-remove support material.
- **Nylon (pSLS)**: Used for the female rotating mechanism due to its strength (for bearing spring tension) and compatibility with heat-set inserts.

## Assembly Instructions

1. Attach the TPU phone case to the nylon female rotating component using four M3 bolts.
2. Insert the spring column into the resin housing and drop the spring onto the column.
3. Secure the spring with the spring lock end piece using an M3 bolt.
4. Mount the assembly onto the bike handlebar using the remaining four M3 bolts.

## Gallery

#### CAD

<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a45becb84638a70c26?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

#### In-use

<img src="assets/img/mount.gif"/>




