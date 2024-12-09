---
layout: page
title: Team Spirit! (Ongoing)
description: Dynamic Obstacle Avoidance and Loco-Manipulation planning for a quadruped
img: assets/img/12.jpg
importance: 2
category: Graduate
related_publications: true
---

### Introduction
Quadruped robots face significant challenges in **dynamic obstacle avoidance and loco-manipulation** due to rapidly changing environments and this has been a prime research topic till now. To address this, we propose the implementation of a PRM planner that supports loco-manipulation tasks by planning in the *z-direction* as well. The proposed **kinodynamic** planner has been tested out in the simulation framework called QUAD-SDK.

### Motivation
The current implementation in the QUAD-SDK stack for the quadruped is the RRT-Connect algorithm that plans in *x* and *y* directions and faces difficulty in navigation through changing its height as shown in the video below.
<div class="text-center">
    <video controls class="img-fluid rounded z-depth-1" preload="metadata" width="600" height="400">
        <source src="/assets/video/Colliding_with_table.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
    <div class="caption mt-2">
        Current shortcoming of the 2-axis RRT-Connect Planner. 
    </div>
</div>

### PRM Implementation:

#### Key Features:
- PRM roadmap precomputed with nodes representing feasible configurations.
- Dynamic obstacle roadmap updates using environment feedback.
- Foothold selection and balance constraints incorporated.
- Adapted *z-axis* height for loco-manipulation tasks, ensuring stable trajectories.

<div class="text-center">
    <video controls class="img-fluid rounded z-depth-1" preload="metadata" width="600" height="400">
        <source src="/assets/video/avoiding_table.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
    <div class="caption mt-2">
        Implementation of PRM Planner
    </div>
</div>
### Results
Performance Metrics:
Path quality: Improved by ~30% compared to RRT-Connect.
Planning time: Reduced by ~20% under high obstacle density.
<div class="row">
    <div class="col-sm mt-3">
        {% include figure.liquid path="assets/img/results_PRM.jpg" title="Comparison: RRT vs PRM" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    EKF Framework and the hardware setup.
</div>

### Visual Demonstration
Below is a video demonstrating the quadruped navigating a dynamic environment using PRM.
<div class="text-center">
    <video controls class="img-fluid rounded z-depth-1" preload="metadata" width="600" height="400">
        <source src="/assets/video/z_demo_works.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
    <div class="caption mt-2">
        Watch the EKF in action, predicting and correcting cloth state in real-time.
    </div>
</div>

### Challenges and Future Work

#### Challenges

- Efficient roadmap updates in highly dynamic scenarios.
- Balancing computational load with real-time requirements.

#### Future Work

- Explore hybrid planners combining PRM and reactive methods.
- Use reinforcement learning to optimize roadmap generation.

