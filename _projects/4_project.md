---
layout: page
title: Semantic ORB SLAM
description: Enhancing ORB-SLAM with semantic segmentation to improve robustness in dynamic environments.
img: assets/img/slam_cover.jpg
importance: 4
category: Graduate
---

### Overview

The **Semantic ORB-SLAM** project integrates semantic segmentation with the ORB-SLAM3 framework to enhance its robustness and accuracy in dynamic environments. By leveraging semantic labels, the system distinguishes between transient and stable elements, prioritizing permanent landmarks for localization and mapping. This innovative approach mirrors human navigation strategies and addresses the limitations of traditional ORB-SLAM implementations in dynamic scenarios.

### Motivation

In dynamic environments, landmarks that move can disrupt localization accuracy. The integration of semantic understanding enables ORB-SLAM to filter out transient objects (e.g., vehicles) and focus on stable features like walls and furniture. This alignment with human-like navigation techniques improves SLAM robustness and reduces computational overhead.


### Methodology

1. **Semantic Segmentation:** 
   - Utilized YOLO v8 and synthetic data from NVIDIA Isaac Sim for precise object segmentation.
   - Segmented images were used to mask dynamic objects and extract features only from relevant, stable objects.

2. **Feature Detection and Matching:**
   - Applied ORB feature detection on semantically segmented frames.
   - Performed nearest-neighbor matching with descriptors to establish reliable correspondences between frames.

3. **Testing and Validation:**
   - Validated the approach using the EuRoC dataset for real-world and synthetic environments.
   - Assessed the system's performance under various viewing angles and object rotations.

### Results

- Achieved robust localization by filtering dynamic objects and focusing on key landmarks.
- Demonstrated that semantic segmentation improves feature detection accuracy and reduces computational load.
- Identified challenges in handling significant object rotations, with future work focusing on geometric consistency checks.

### Future Work

- Incorporate advanced geometric consistency methods for improved feature matching.
- Extend the system to dynamic environments with real-world data.
- Explore the integration of semantic SLAM in urban navigation and assistive robotics.

---

### Media

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/orb_slam_2.jpg" title="Segmented Image with Key Features" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/orb_slam_1.jpg" title="Synthetic Data from NVIDIA Isaac Sim" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

<div class="row mt-3">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/orb_slam_3.jpg" title="Feature Matching Results" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

---

### References

- Campos, C., et al., “ORB-SLAM3: An Accurate Open-Source Library for Visual, Visual-Inertial, and Multimap SLAM,” *IEEE Transactions on Robotics*.
- Zhang, J., et al., “VDO-SLAM: A Visual Dynamic Object-Aware SLAM System,” *arXiv preprint*.
- Redmon, J., et al., “YOLO: Unified, Real-Time Object Detection,” *arXiv preprint*.

---

This project showcases the potential of combining semantic understanding with traditional SLAM frameworks to revolutionize robotic navigation in complex, dynamic environments.
