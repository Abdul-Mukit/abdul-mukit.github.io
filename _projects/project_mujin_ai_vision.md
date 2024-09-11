---
layout: page
title: AI Robot Vision
description: Deep learning and classical computer vision based perception software for warehouse automation.
img: assets/img/mujin/robot.png
importance: 1
category: work
related_publications: true
---

#### Introduced AI Vision System for Robotic Depalletization [@Mujin](https://mujin-corp.com/depalletizing/)
* Developed and deployed the first deep learning assisted robotic vision system for depalletizing applications.
* Currently being used in companies like Walmart, P&G, Paltac, ebabling thousands of picks per day.
* Developed, trained, and deployed an instance segmentation model using PyTorch and ONNX to production.
* Developed 6-DoF pose estimation and geometric vision pipeline using OpenCV and Point Cloud Library.
* Optimized vision system to run on CPU at 2-FPS and integrated with robotic system enabling 700 picks per hour.

#### Package Condition Sensitive Point Cloud Filtering
* Implemented package condition (damaged or tilted) estimation algorithm for cardboard boxes and packs of cans.
* Developed 3D point cloud filtering algorithms for damaged and tilted items using OpenCV and PCL.
* Integrated vision algorithms to robotic systems at Walmart warehouses enabling damaged and tilted item handling.


<!-- Application Description -->
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/video/single_sku_depal_with_detection_view.gif" class="img-fluid rounded z-depth-1" controls=false autoplay=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/video/pallet_detection_and_placed_on_a_splitsheet.gif" class="img-fluid rounded z-depth-1" controls=false autoplay=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/video/quickbot_with_digital_twin.gif" class="img-fluid rounded z-depth-1" controls=false autoplay=true %}
    </div>
</div>
<div class="caption">
    A robot has to detect and pick, non-stop every day. A depal robot has to pick infinite variations of boxes, pallets, anti-slip sheets, and packs of cans. The vision system has to update the digital twin in real time for the robot to operate.
</div>


<!-- Problem Description -->
I joined as the first Computer Vision Engineer at Mujin-US in 2023. Before I joined, for the past decade, Mujin had traditionally been a 100%
geometric computer vision-based company. No machine learning, no deep learning. Previous attempts at using Deep Learning for vision
purposes were unsuccessful. However, it had become abundantly clear to Mujin that geometric computer vision alone is struggling
to keep up with the endless complexities and chaotic realities of US warehouses (Yes, US only. Warehouses in Japan are extremely clean and organized).


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/mujin/damaged_boxes_stacked.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/mujin/damaged_box_pointcloud.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/video/tilted_box_picking.gif" class="img-fluid rounded z-depth-1" controls=false autoplay=true %}
    </div>
</div>
<div class="caption">
    Warehouse automation is highly challenging. Left: Boxes often get damaged during transportation. Middle: Point cloud of
    the damaged boxes is often either missing portions or is extremely noisy. Right: Boxes or items can become tilted for whatever reason (including the operator just
    casually throwing some boxes on top so that the robot picks them too. Yes that happens!). Guess what! Robot can't stop. Vision has to work.
</div>


<!-- Solution -->
I am an avid follower of Dr. [Andrew Ng](https://youtu.be/5p248yoa3oE?si=3EnW7_ZcvCHvnYFH), one of the pioneers of Deep Learning. Equipped with Dr. Andrew Ng's teachings from 
[Deep Learning Specialization](https://www.deeplearning.ai/courses/deep-learning-specialization/) and
[Machine Learning in Production](https://www.deeplearning.ai/courses/machine-learning-in-production/) courses, I was perfectly positioned at Mujin. Within a few months, I was able to introduce the first AI vision system that outperformed Mujin's geometric vision system of the past decade both in terms of speed and detection accuracy. The new system was nearly 99% accurate while being nearly 10x faster than our existing vision system. Currently, I am leading the R&D of a hybrid vision system that takes advantage of the unique strengths of both AI and geometric vision.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/mujin/instance_seg_1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/mujin/instance_seg_2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/mujin/instance_seg_3.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Real-time instance segmentation and 6-DoF pose estimation enabled by deep learning.
</div>
