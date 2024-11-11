---
layout: distill
title: Mobility and Incident Management in Urban Systems
description: AI-driven methods to provide traffic impact for immediate, near-future, and long-term period, aiding mobility and incident management process.
tags: AI operation planning
giscus_comments: false
date: 2024-07-23
featured: true
thumbnail: assets/img/mobility-0.jpeg

# authors:
#   - name: Albert Einstein
#     url: "https://en.wikipedia.org/wiki/Albert_Einstein"
#     affiliations:
#       name: IAS, Princeton
#   - name: Boris Podolsky
#     url: "https://en.wikipedia.org/wiki/Boris_Podolsky"
#     affiliations:
#       name: IAS, Princeton
#   - name: Nathan Rosen
#     url: "https://en.wikipedia.org/wiki/Nathan_Rosen"
#     affiliations:
#       name: IAS, Princeton

# bibliography: 2018-12-22-distill.bib

# Optionally, you can add a table of contents to your post.
# NOTES:
#   - make sure that TOC names match the actual section names
#     for hyperlinks within the post to work correctly.
#   - we may want to automate TOC generation in the future using
#     jekyll-toc plugin (https://github.com/toshimaru/jekyll-toc).
# toc:
#   - name: DT in Safety
#     # if a section has subsections, you can add them as follows:
#     # subsections:
#     #   - name: Example Child Subsection 1
#     #   - name: Example Child Subsection 2
#   - name: DT in Emission
#   - name: DT in Emergency
# Below is an example of injecting additional post-specific styles.
# If you use this post as a template, delete this _styles block.
_styles: >
  .fake-img {
    background: #bbb;
    border: 1px solid rgba(0, 0, 0, 0.1);
    box-shadow: 0 0px 4px rgba(0, 0, 0, 0.1);
    margin-bottom: 12px;
  }
  .fake-img p {
    font-family: monospace;
    color: white;
    text-align: left;
    margin: 12px 0;
    text-align: center;
    font-size: 16px;
  }
---

In today's data-driven world, transportation researchers are using advanced technologies to tap into the enormous potential of video data for urban management. As the Federal Highway Administration (FHWA) notes, this data is being applied to a variety of areas such as system planning, operations, safety monitoring, and infrastructure condition assessments.

By combining video data with cutting-edge AI and deep learning methods, we can unlock a new stream of valuable information. This enables cities to become "machine eyes" for real-time insights, allowing us to monitor urban environments with unprecedented detail and precision.

Imagine a city equipped with intelligent sensing systems—tracking traffic, detecting congestion points, monitoring safety hazards, and even assessing infrastructure wear and tear—all in real-time. With this automation, we can shift from static datasets to dynamic, continuous flows of information that lead to smarter, faster, and more efficient decision-making.

The figure below illustrates how **Urban Sensing Systems** collect and process data from multiple domains, such as pedestrian movement, traffic conditions, parking availability, freight logistics, emergency response, and environmental monitoring. AI-powered video analysis enables these systems to provide actionable insights, empowering city planners and transportation managers to make informed decisions that improve safety, mobility, and quality of life.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/smartsensing-0.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Multiple usage of traffic sensing in daily urban system.
</div>

In the realm of urban management, enhancing situational awareness is crucial to improving decision-making processes. My research aims to answer the pressing question: 
> How can existing urban sensors be optimized to enhance situational awareness across large-scale urban systems? 

By focusing on accuracy, cost-efficiency, and resiliency, my work seeks to push the boundaries of what urban sensing systems can achieve.

On the detection side, a deep-learning-based work zone object detection model using a data-centric approach is developed. This method iteratively improves the model’s performance by augmenting a custom training dataset from multiple sources, overcoming the challenge of sparse annotated real-world work zone images. With this in place, I then explore how existing traffic sensors can be effectively deployed to gain real-time traffic information. One focus of my research is on the flexibility of smart sensors. These sensors are often limited by power constraints, forcing a trade-off between data collection duration and accuracy/resolution. To address this, a learning-based framework that strategically determines observation timings for battery-powered devices is developed. This approach reconstructs full data streams from sparsely sampled observations, minimizing performance loss while significantly extending the system's lifetime.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/smartsensing-1.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    How to use the existing pan-tilt-zoom cameras installed along each intersection to return network-level situational awareness?
</div>

Another aspect of my research addresses the **underutilization of urban traffic cameras**. While cities often have wide coverage of traffic cameras along road segments and intersections, these cameras are typically only used when nearby accidents occur. Most of the time, they remain idle. 
> How can we transform the underutilized network of urban traffic cameras into a cooperative, real-time, and network-wide traffic sensing system to enhance the overall efficiency of urban traffic monitoring and management?

To maximize the utility of these deployed cameras, I developed a **distributed and cooperative framework** that allows them to work together and provide network-wide traffic information. This dramatically enhances the cost-efficiency of existing urban sensing systems.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/smartsensing-2.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    If some of the current sensors go down, can the rest of traffic sensors (no matter what type) work with each other and stay resilent to such malfunction situation?
</div>

Lastly, my research extends beyond traffic cameras to explore collaboration with other sensing techniques, including pavement-invasive detectors (e.g., inductive loops, magnetometers) and non-pavement-invasive detectors (e.g., microwave radar, ultrasonic sensors). A key question I address is: 
> What happens when some sensors malfunction? Can the remaining sensing systems cooperate to still provide satisfactory performance? 

My work seeks to build a resilient sensing network where failures in individual sensors do not compromise the overall system’s capability.


## Resources
- Tao Li, **Zilin Bian***, Haozhe Lei, Fan Zuo, Ya-Ting Yang, Quanyan Zhu, Zhenning Li, Kaan Ozbay.
  **Multi-level traffic-responsive tilt camera surveillance through predictive correlated online learning.**
  Transportation Research Part C: Emerging Technologies 167 (2024): 104804.
- Tao Li, **Zilin Bian***, Haozhe Lei, Fan Zuo, Ya-Ting Yang, Quanyan Zhu, Kaan Ozbay.  
  **"Enhancing Network-Wide Situational Awareness through Passive and Proactive Online Control: A Graph-Based Transformer Approach for Resilient Urban Sensing Systems."**  
  Details coming soon.
- Fan Zuo, Jingqin Gao, Kaan Ozbay, **Zilin Bian**, Daniel Zhang.
**Urban Work Zone Detection and Sizing: A Data-Centric Training and Topology-Based Inference Approach.**
In 2023 IEEE 26th International Conference on Intelligent Transportation Systems (ITSC), pp. 3235-3240. IEEE, 2023.
- Ruixuan Zhang, Wenyu Han, **Zilin Bian**, Kaan Ozbay, Chen Feng.
**Learning When to See for Long-term Traffic Data Collection on Power-constrained Devices**
In 2023 IEEE 26th International Conference on Intelligent Transportation Systems (ITSC), pp. 3235-3240. IEEE, 2023.

---
