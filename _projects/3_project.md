---
layout: page
title: Autonomy Intern @ Oshkosh
description: End-to-End implementation of Semantic Segmentation   
img: assets/img/3.jpg
importance: 2
category: Graduate
related_publications: false
---

### Semantic Segmentation for Autonomous Vehicles  
During my internship at **Oshkosh Corporation's Autonomy Team**, I focused on developing and deploying **semantic segmentation models** for advanced perception in autonomous vehicles. This project involved creating robust segmentation systems capable of identifying road elements, vehicles, pedestrians, and other critical objects in real-time. Scripted ROS2 nodes to integrate the model in the stack, performance was tested with NVIDIA Orin device. 

### **Key Contributions**
- **Model Development:**  
  Implemented and fine-tuned deep learning segmentation models for real-time object detection and segmentation.    
- **Optimization:**  
  Implemented **TensorRT acceleration** for deployment on NVIDIA Orin platforms, reducing inference latency by 30%.  
- **Integration:**  
  Integrated the segmentation module into the existing **Autonomy stack** for enhanced autonomous navigation and tested on vehicle.  

### **Challenges and Achievements**
- **Challenge**  
  Optimizing segmentation models to handle **dynamic urban environments** (e.g., moving vehicles, changing lighting conditions).  
- **Achievement**  
  Achieved **>90% mIoU (mean Intersection over Union)** on the custom dataset with a lightweight architecture, meeting real-time performance requirements.

### **Impact**
The developed segmentation system significantly improved **object detection accuracy** and **path planning reliability** for autonomous vehicles. This work contributed to Oshkosh's ongoing efforts in advancing autonomous vehicle technology for various applications.

### **Demo Video**
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3">
        <video controls width="100%">
            <source src="assets/videos/quadruped_navigation.mp4" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </div>
</div>
<div class="caption">
    Demonstration of the quadruped navigating a dynamic environment using PRM.
</div>
