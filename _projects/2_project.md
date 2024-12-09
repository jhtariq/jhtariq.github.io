---
layout: page
title: Real-Time Cloth State Estimation (Ongoing)
description: Estimation and Prediction of Cloth Dynamics for Robotic Manipulation using EKF
img: assets/img/ekf_cover.jpg
importance: 1
category: Graduate
related_publications: true
---

### Cloth State Estimation Using EKF 
This project focuses on estimating the state of deformable cloth using an **Extended Kalman Filter (EKF)**. Estimating the state of cloth is critical for robotic manipulation tasks involving fabrics, enabling precise control and interaction with deformable objects. The system combines a physics-based prediction model with real-time observations from AprilTags to achieve accurate state estimation.

---

### **Objectives**

- Develop a robust EKF-based framework for tracking the state of cloth.
- Integrate a physics prediction model (CIPC) for cloth dynamics.
- Utilize AprilTags for real-time observations to refine the state estimation.
- Minimize latency to meet real-time requirements.

### **Implementation Overview**

- **Observation Model**  
  - AprilTags are used to gather the real-time positions of markers attached to the cloth.
  - Observations are processed to correct the predicted state of the cloth.

- **Prediction Model**  
  - A physics-based model, CIPC (Compliant Implicit Physics Constraints), predicts the cloth’s state based on dynamics and applied forces.
  - EKF incorporates these predictions to maintain a probabilistic representation of the cloth's state.


### **Key Features**

- **Low Latency**: The EKF implementation achieves a processing latency of ~ 0.7 seconds, enabling real-time update  
- **Simulation to Reality**: Incorporates physical constraints to bridge the gap between simulation and real-world manipulation  
- **Scalable Framework**: Can be extended for applications beyond cloth manipulation, such as flexible or articulated objects  


### **Results**

- **Accuracy**: Demonstrated significant improvement in tracking precision compared to standard filtering techniques.  
- **Robustness**: The system performs reliably even with partial or noisy observations.  

<div class="row">
    <div class="col-sm mt-3">
        {% include figure.liquid path="assets/img/ekf_hwr.jpg" title="Comparison: RRT vs PRM" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    EKF Framework and the hardware setup.
</div>

### **Video Demonstration**

<!-- <video controls class="img-fluid rounded z-depth-1">
    <source src="assets/video/output_real.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

<div class="caption">
    Watch the EKF in action, predicting and correcting cloth state in real-time.
</div> -->
<!-- <video controls class="img-fluid rounded z-depth-1" preload="metadata" width="600" height="400">
    <source src="/assets/video/output_real.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

<div class="caption">
    Watch the EKF in action, predicting and correcting cloth state in real-time.
</div> -->
<div class="text-center">
    <video controls class="img-fluid rounded z-depth-1" preload="metadata" width="600" height="400">
        <source src="/assets/video/output_real.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
    <div class="caption mt-2">
        Watch the EKF in action, predicting and correcting cloth state in real-time.
    </div>
</div>
