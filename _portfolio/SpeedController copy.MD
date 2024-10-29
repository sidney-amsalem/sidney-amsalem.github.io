---
title: "Autonomous Vehicle Speed Controller"
excerpt: "An autonomous speed controller that adapts to various traffic conditions."
header:
  image: /assets/img/speed-controller.png
  teaser: /assets/img/speed-controller.png
gallery:
   
---

# Autonomous Vehicle Speed Controller

## Overview

Our autonomous vehicle speed controller is designed to reduce traffic waves, improve fuel efficiency, and consider user preferences in speed, acceleration rate, and following distance for freeway driving scenarios. It adapts to various traffic conditions, from free-flowing to bumper-to-bumper traffic.

## Key Features

- **Adaptive Control**: Adjusts to different traffic conditions
- **User Customization**: Considers user preferences for speed, acceleration, and following distance
- **Safety-Focused**: Maintains safe following distances and responds to lead vehicle presence
- **Fuel Efficiency**: Aims to reduce unnecessary acceleration and braking
- **Traffic Wave Reduction**: Designed to mitigate phantom traffic jams

## Technical Details

### Inputs
- Velocity of the ego vehicle
- Space gap to the lead vehicle
- Relative velocity to the lead vehicle

### User Preferences
- Maximum speed
- Acceleration rate
- Following distance preference

### Key Calculations
1. **Time Gap Calculation**: 
   - Starts with 2 seconds at 30mph
   - Increases by 1 second per 8/10/15 mph increase (user-selectable)

2. **Speed Control**:
   - Accelerates at a constant rate of 2.2 m/s² when below max speed and no lead vehicle
   - Sets acceleration to zero when at max speed to maintain constant speed

3. **Following Distance Control**:
   - Adjusts acceleration based on the difference between desired and actual time gap
   - Uses a square root function to prevent large acceleration values

## Controller Design

![Controller Design](speed-controller.png)

Our controller uses three 3-way switches for user customization:
1. Lead distance calculation
2. Velocity input
3. Acceleration rate factor

The controller calculates the time gap, compares it to the desired time gap, and determines the appropriate acceleration. A speed limiter ensures the vehicle doesn't exceed the user-set maximum speed.

## Performance Analysis

We tested our controller on a freeway and analyzed its performance using ROS bag data. Key observations include:

1. **Responsiveness**: The controller actively adjusts acceleration based on lead vehicle presence and distance.
2. **Speed Maintenance**: Maintains speeds above 40 mph while responding to changes in traffic conditions.
3. **Safety**: Rapidly decelerates when lead distance decreases significantly.
4. **Smooth Operation**: Resists overly aggressive responses to appearance or disappearance of lead vehicles.

## Validation

Our controller was successfully tested in real-world conditions. You can view a video of our test run [here](https://youtu.be/7MECVVMF_n8).

## Future Work

To further validate the benefits of our controller, we propose:
- Extensive testing to measure its impact on phantom traffic jams
- Safety improvement assessments
- User studies to evaluate increased usage due to customizability

## Code Repository

All supporting code for this project is available in our [GitHub repository](https://github.com/aarnab18/teamasa).

## Conclusion

Our autonomous vehicle speed controller offers a promising solution for improving traffic flow, enhancing safety, and increasing user satisfaction in freeway driving scenarios. With its adaptive nature and user-centric design, we believe it has the potential to significantly impact rush hour traffic and provide a more comfortable driving experience.