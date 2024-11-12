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

In our rapidly urbanizing world, ensuring smooth and safe mobility within cities is a complex challenge, made more pressing by the increasing frequency of unexpected disruptions and incidents on the road. My research in urban mobility and incident management focuses on leveraging **spatio-temporal modeling** techniques, by making analogies between ``road network and its topological elements``, 
to improve real-time, near-future, and long-term situational awareness and response capabilities for urban transportation systems. By developing tools that enable proactive management and resilience in the face of congestion and incidents, I aim to enhance both the safety and efficiency of urban mobility networks.

Traffic incidents, such as accidents and work zones, introduce significant challenges to urban transportation systems, often resulting in congestion, delays, and cascading disruptions that affect a wide area. These incidents not only hinder the flow of traffic but also create heightened safety risks, as congestion and delays can increase the likelihood of secondary accidents.

My research begins by investigating the impact of traffic incidents on urban transportation systems. For example, I applied Artificial Neural Networks (ANN) and Monte Carlo Dropout to quantify the uncertainty associated with reduced road capacity due to work zones. Expanding to unexpected traffic accidents, I first developed an adaptive Bayesian network method to predict accident duration, providing valuable insights for incident response. Building on this, I designed a stacked autoencoder (SAE) combined with Long Short-Term Memory (LSTM) networks to analyze traffic flow patterns influenced by accidents. Recognizing the importance of both spatial and temporal correlations, I then expanded my research to model traffic networks as graphs, effectively capturing how traffic flows propagate along connected road segments. To further enhance temporal understanding, I integrated road capacity data into a Graph Convolutional Network (GCN) paired with a Temporal Convolution Network (TCN), allowing the model to better learn time-dependent traffic dependencies.
To further advance prediction capabilities, I developed a Multi-Scale Graph Wavelet Network with Temporal Convolution (MSGWTCN), which leverages graph wavelet properties to continuously adjust its scales during the learning process. This adaptive scaling allows MSGWTCN to effectively capture both short-range and long-range traffic propagation, providing a more nuanced understanding of spatial patterns and temporal sequences. 

Beyond immediate situational awareness of traffic flow and congestion, my research also explores how traffic incidents might affect traffic in the near future and over the long term. To address this, I designed a data-driven framework that learns from empirical patterns of traffic impacts caused by pre-planned work zones, using machine learning models to provide predictive insights. This framework forecasts the potential impacts of upcoming or scheduled work zones based on planned road closure details and their spatial-temporal characteristics, such as location, start/end time, and duration. The framework has been deployed as a web-based tool, the Data-driven Work Zone Impact and Conflict Estimation platform ([DWICE](https://c2smarter.engineering.nyu.edu/developing-a-multi-agency-multi-modal-construction-management-software-tool-to-enhance-coordination-of-construction-projects-city-wide-during-planning-and-operation-phases/)), which is currently utilized by the New York State Department of Transportation (NYSDOT) to support more informed planning and impact mitigation. 



## Resources
- **Zilin Bian** and Kaan Ozbay. **Estimating uncertainty of work zone capacity using neural network models.** Transportation Research Record 2673 (2019): 49-59.
- **Zilin Bian**, Kaan Ozbay and Abdullah Kurkcu. **Travel time uncertainty prediction in the presence of non-recurrent traffic congestion.** Accepted in 99th Annual Meeting of the Transportation Research Board (TRB 2020).
- **Zilin Bian**, Dachuan Zuo, Jingqin Gao, Kaan Ozbay, Zhenning Li. **Informed along the road: roadway capacity driven graph convolution network for network- wide traffic prediction.** Accepted in IEEE Intelligent Transportation Systems Conference (ITSC 2024). [link](https://arxiv.org/abs/2406.13057)
- **Zilin Bian**, Dachuan Zuo, Jingqin Gao and Kaan Ozbay. **Adaptive traffic incident duration prediction: a hybrid approach of change detection and Bayesian network.** Transportmetrica A: Transport Science, under revision.
- **Zilin Bian**, Jingqin Gao, Kaan Ozbay and Zhenning Li. **Traffic prediction considering multiple levels of spatial-temporal information: a multi-scale graph wavelet-based approach** Transportmetrica B: Transport Dynamics, under review. [link](https://arxiv.org/abs/2406.13038)


---
