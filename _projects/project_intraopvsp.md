---
layout: page
title: IntraOpVSP
description: Intra operative virtual surgical planning using AR and Computer Vision.
img: assets/img/intraopvsp/head_in_ghost_mode.png
importance: 2
category: work
related_publications: false
---

A set of mixed-reality apps that allow surgeons to anatomically align and interact with CT scan data through Microsoft Hololens. The technology has been used in over 50 human surgeries. The technology has been licensed to a startup for [commercialization](https://www.xironetic.com/) and has been approved by [FDA](https://www.businesswire.com/news/home/20221114005198/en/Xironetic-Receives-FDA-Clearance-for-Augmented-Reality-Surgical-Software).  

#### My Contributions
As part of my [MS research](https://shareok.org/handle/11244/332567), I implemented the technology from scratch.
* Developed mixed reality software using Unity, Mixed Reality Toolkit, and Microsoft Hololens-2.
* Used OpenCV, DLib, and PyTorch for 6-DoF pose estimation of human head and surgical tools.
* Annotated 2D, 3D data for machine learning.

**Skills/Tools:** PyTorch, OpenCV, Unity3D, Blender, MeshLab, DLib, C++, C#, Python.  


<div align="center">
    {% include video.liquid path="https://www.youtube.com/embed/kwTxmF2W0vY" class="img-fluid rounded z-depth-1" %}
</div>
<div class="caption">
    IntraOpVSP live demonstration.
</div>


<!-- Problem Description -->
#### The Problem
The mission is to augment every surgery. Compared to a pilot flying a plane or even a regular google-map user on his way to work/home, surgeons today have their instruments clustered behind them hanging in the wall. The Google Maps user or the pilot gets constant real-time updates regarding where they are, what to do next, and other vital data that helps them make split-second decisions. They don't have to plan the trip for days or memorize every turn and detail of every landmark along the way. They just do it. On the other hand, surgeons today have to do rigorous surgical planning, memorize the specifics of each unique case, and all the necessary steps to ensure the safest possible surgery. Then they engage in complex procedures for several hours, with no targeting or homing devices or head-mounted displays to assist them. They have to feel their way to their objective and hope everything goes as they planned. In my research, I made the "google-maps" for surgery.   


#### Examples:
Following are IntraOpVSP usage examples:  


<!-- CT Before After Views -->
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/intraopvsp/ct_view_all.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/intraopvsp/ct_view_base.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/intraopvsp/ct_view_post.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    CT scan of the head can be aligned to the patient's head using computer vision. Purple shows the CT scan of the head before surgery. Red shows the planned cuts/segments and their intended position after the surgery. Yellow shows the base structure of the skull which will remain unmodified.
</div>



<!-- Vision -->
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/intraopvsp/amira_annotation.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/intraopvsp/dlib_face.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/intraopvsp/head_aligned_to_real_patient.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Face keypoints on the CT scan are annotated and loaded in IntraOpVSP before surgery. Using Dlib, ICP and on-board cameras in Hololens-2 the 6-DoF pose of the head is estimated. Then using Unity3D, the CT scan is aligned with the subject's head during surgery.
</div>



<!-- CT Parts Moving-->
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/intraopvsp/ct_parts_moving_1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/intraopvsp/ct_parts_moving_2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Using hand tracking and voice commands, the user can interact with the different parts of the aligned CT scans.
</div>



<!-- CT Slice Views -->
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/intraopvsp/ct_view_slice_1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/intraopvsp/ct_view_slice_2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/intraopvsp/ct_view_slice_3.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The surgeon can use their hand to slice the CT scan data and create a cross-sectional view. This view helps surgeons get an idea of how thick a section is as they often need to drill or cut.
</div>



<!-- Liver Surgery -->
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/intraopvsp/surgery_liver_1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/intraopvsp/surgery_liver_alignment_1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/intraopvsp/surgery_liver_alignment_2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This is a demonstration of liver surgery. Computer vision can't be used for pose estimation as the body of the subject is covered by a cloth. Thus, I implemented a semi-automatic alignment process by allowing the surgeon to place known landmarks on the subject's body during surgery. I then align the CT scan data to the subject's body using 3D rigid body pose transform estimation.
</div>



<!-- Liver Surgery Tumor -->
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/intraopvsp/surgery_liver_2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/intraopvsp/surgery_liver_3.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/intraopvsp/surgery_liver_4.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Example of liver tumor removal. 
</div>



<!-- Ear Reconstruction Surgery -->
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/intraopvsp/surgery_ear_1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/intraopvsp/surgery_ear_2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Example of an ear reconstruction surgery using IntraOpVSP.
</div>
