---
layout: distill
title: Digital Twins in urban decision science
description: How does Digital Twin (DT) help the management process in daily urban system? My research aims to answer this question in terms of enhancing travelers' safety, urban sustainability and emergency response.
tags: digital-twins AI operation
giscus_comments: false
date: 2024-09-06
featured: true
thumbnail: assets/img/digitaltwin-background-1.png
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
toc:
  - name: DT in Safety
    # if a section has subsections, you can add them as follows:
    # subsections:
    #   - name: Example Child Subsection 1
    #   - name: Example Child Subsection 2
  - name: DT in Emission
  - name: DT in Emergency
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

## DT in Safety

> ##### Research Question:
>
> While congestion is easily observed and captured by sensors for traffic operators, what about the driving risks (e.g., near-miss, hard braking) experienced by drivers? 
> Can they leverage this information to improve traffic management?
{: .block-warning }

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/crash.png" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/congestion.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


Urban mobility management is vital for ensuring efficient movement in cities, improving transportation systems, and enhancing quality of life. However, current strategies often focus on high-level traffic data while overlooking critical safety risks faced by road users, such as driving hazards and road conflicts. Acquiring safety risk information usually relies on vehicle-based sensing devices, such as advanced onboard equipment (OBE) installed in connected and automated vehicles (CAVs), which can capture real-time driving situations like hard braking, acceleration, and near-miss events. 

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cav-dashview.gif" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    OBE risk detection in CAVs
</div>

However, the current implementation of **CAVs** and vehicle-based sensing devices in large-scale transportation systems is still `limited`. This gap between management perspectives and driver experiences calls for a more integrated approach that addresses both mobility and safety concerns.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/DT-DIMA Concept_v2.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    A feedback loop that effectively communicates driver-centric information to transportation managers, thereby enabling more informed, driver-aware decision-making in considering not only mobility risks but also safety risks.
</div>

Enter the **Digital Twin (DT) technology**. A DT creates a virtual model of the physical transportation system, allowing for real-time monitoring, prediction, and optimization. By integrating DTs into urban mobility management, we can bridge the disconnect between traffic oversight and driver safety. My research proposes the DT-based Driver risk-aware Intelligent Mobility Analytics (**DT-DIMA**), a DT-based framework designed to incorporate real-time driver-centric information into decision-making processes.

Key innovations of this system include using pan-tilt cameras (PTCs) as cost-efficient sensors, capable of capturing and replicating real-world traffic conditions across large urban networks. This data feeds into predictive models that assess both mobility risks (e.g., traffic flow and speed) and safety risks (e.g., driving hazards), offering a comprehensive view of road conditions.

---

## DT in Emission

> ##### Research Question:
>
> Greenhouse gas (GHG) emissions are typically measured using fixed monitoring stations, providing insights at a regional or macroscopic level. However, emissions vary significantly based on vehicle type, size, model year, and more. So how can we monitor GHG emissions at a high-resolution, granular level and use this data to improve transportation and environmental management?
{: .block-tip }

Current approaches to monitoring greenhouse gas (GHG) emissions largely rely on fixed measurement stations, which provide regional or macroscopic data. While useful for broad assessments, these stations fall short in capturing the nuances of emissions at a more granular level. Vehicle emissions can vary greatly depending on factors like vehicle type, size, fuel type, model year, and driving behavior. This variability is critical for understanding the real impact of transportation on air quality, especially in urban areas where traffic conditions are highly dynamic. The current gap lies in the inability to monitor emissions at a high-resolution level, which limits the potential to make informed decisions about local environmental and traffic management.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/dt-emission-0.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/dt-emission-1.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption"> 
    GHG simulation picture was referenced to the post: [If New York’s carbon emissions were solid, they’d bury the Empire State Building within a day](https://grist.org/climate-energy/if-new-yorks-carbon-emissions-were-solid-theyd-bury-the-empire-state-building-within-a-day/).
</div>


High-resolution emission monitoring is essential for bridging this gap. By capturing detailed, real-time data about individual vehicles and their emissions, transportation managers and environmental policymakers can better understand the distribution of pollutants across different areas and times of day. This detailed data can reveal patterns that are invisible at the regional level, such as localized hotspots of high emissions during peak traffic hours or in areas with frequent congestion. Such insights would enable more targeted interventions, such as adjusting traffic flow, optimizing signal timing, or even implementing dynamic emission-based pricing to reduce pollution in critical areas. Moreover, understanding the specific emission profiles of different vehicle types can support more effective policy measures, such as incentivizing the use of cleaner vehicles or updating emissions standards for certain categories of vehicles.

Our solution of achieving high-resolution emission monitoring lies in the integration of Digital Twin (DT) technology, AI methods, and smart sensors. Digital twins create a virtual model of real-world transportation networks, allowing for real-time simulation and analysis of traffic and emissions. By leveraging wide-coverage cameras already deployed along urban roads, we use computer vision methods to extract vehicle type, speed, and aggregated link-based traffic flow, estimate their emissions based on characteristics such as type and driving behavior, then we use graph neural networks (GNNs) to scale up to network-level, and feed this data into a digital twin system. This integration provides transportation managers with a real-time, high-resolution view of emissions across the network, enabling them to make informed decisions that improve both traffic flow and air quality. Digital twins, with their capacity for real-time prediction and optimization, offer high-resolutional monitoring information for managing urban mobility and environmental impact simultaneously.

---

## DT in Emergency

> ##### Research Question:
>
> How can high-fidelity Digital Twin systems, integrating AI and smart sensors, transform traditional emergency management by providing real-time, detailed situational awareness before and during emergencies, thereby enhancing the efficiency and effectiveness of response teams?
{: .block-danger }

Man-made disruptions such as major traffic accidents and infrastructure failures similar to the collapse of Baltimore’s Francis Key Bridge in urban areas, particularly in densely populated regions like the New York-New Jersey (NYNJ) region, present substantial challenges for emergency management, leading to severe network-wide congestion, delays, and potentially life-threatening injuries and fatalities. The unpredictable and complex nature of such incidents requires advanced predictive technologies to effectively manage disruptions and mitigate their impact. 

Traditional emergency response approaches often depend on human reporting or fixed camera feed, which provide limited, point-specific information and fail to capture comprehensive details of the surrounding environment, such as road layouts and real-time traffic conditions that are continuously changing due to the incident dynamics as well as response measures by emergency management crews. These limitations highlight the need for innovative solutions that are capable of providing detailed and comprehensive situational awareness to drastically improve real-time emergency response capabilities. 

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/nanodt-concept-0.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    NanoDT for emergency management in response to highly disruptive occurrences in urban areas.
</div>

Digital Twin (DT) technology provides a powerful tool for replicating real-world transportation systems, aiding traffic accident management at both micro and macro levels. DTs have been effective in capturing vehicle trajectories, supporting traffic management, visualizing infrastructure, vehicle movements, and predicting traffic conditions. However, high-fidelity 3D simulations in DTs are underexplored but essential for offering emergency responders comprehensive awareness. To address this, we introduce the Nano Digital Twin (NanoDT), a cost-efficient approach that integrates broad 2D traffic analysis with focused 3D simulations around accident scenes. The proposed NanoDT targets driving risks, pedestrian conflicts, lane data, and spatial details, enabling real-time, detailed visualizations without overloading computational resources. This enhances Transportation Management Centers’ (TMCs) response capabilities, improving safety and infrastructure resilience in complex urban environments.


<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/nanodt-video-1.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
</div>
<div class="caption">
    A quick example of cosimulation of CARLA (left) and SUMO (right).
</div>

---
## Resources
- {% reference li2024digital %} [paper](https://arxiv.org/pdf/2407.15025)

- Tao Li, **Zilin Bian***, Haozhe Lei, Fan Zuo, Ya-Ting Yang, Quanyan Zhu, Kaan Ozbay.  
  **"Leveraging Digital Twins and AI for High-Resolution Greenhouse Gas Emission Monitoring in Urban Transportation Networks."**  
  Details coming soon.

- **Zilin Bian***, Haozhe Lei, Fan Zuo, Shuo Zhang, Tao Li, Ya-Ting Yang, Semiha Ergan, Kaan Ozbay.  
  **"Harnessing Physics-Informed Traffic Prediction and Digital Twin Technology for Next-Generation High-Fidelity Emergency Management in Urban Networks."**  
  Details coming soon.