---
layout: page
title: Optimal Control Strategy for an Acrobot
description: Utilizing Direct Collocation (DIRCOL) for dynamic trajectory planning and control in a two-link acrobot.
img: assets/img/12.jpg
importance: 5
category: Graduate
related_publications: true
---

### Overview

This project explores the development of an Optimal Control Strategy for an acrobot designed to perform trapeze-style jumping. By employing **Direct Collocation (DIRCOL)** methods, the acrobot was programmed to swing, release, and catch successive trapeze bars with precise control. The system dynamics and constraints were carefully modeled to reflect real-world scenarios, and a quadratic cost function was optimized for energy efficiency and trajectory accuracy.

---

### Objectives

- Develop a robust control strategy for an under-actuated two-link robot.
- Enable the acrobot to perform dynamic transitions between swinging and flying phases.
- Optimize the system using **free-time** intervals for enhanced trajectory precision.
- Minimize energy consumption while achieving smooth motion.

### Dynamics Modeling

The acrobot is modeled as a two-link robot with:
- Revolute joints connecting the links.
- A gripper as the end effector.
- Swinging and flying phases were analyzed separately.

Key equations were derived using the **Euler-Lagrange formulation**

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/acrobot_swing.jpg" title="Swinging Phase" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">The acrobot gathering momentum in the swinging phase.</div>

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/acrobot_flight.jpg" title="Flying Phase" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">The acrobot in the flying phase, heading to the next bar.</div>

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/acrobot_trajectory.jpg" title="Trajectory Visualization" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">Optimized trajectory plotted for both phases.</div>

### Highlights

- **Free-Time Optimization:** The system dynamically adjusted phase durations, improving efficiency.
- **Trajectory Accuracy:** Achieved seamless transitions between trapeze bars.
- **Energy Efficiency:** Quadratic cost functions minimized control efforts.
