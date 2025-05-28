---
layout: page
title: research
permalink: /research/
description: overview of my research and selected projects
nav: true
nav_order: 1
toc:
  sidebar: true
---

<!-- <iframe width="100%" height="800" src="/assets/pdf/research_overview.pdf"> -->

<!-- <img width="100%" height="500" src="/assets/img/.jpg"> -->

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/research_overview.jpg" title="My research overview" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    An overview of my research for developing safe and explainable robots that interact with humans.
</div>

#### **NEURO-SYMBOLIC AI**

---

<div class="row">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/publication_preview/ral_iros2021.png" title="reward modeling" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm-8 mt-3 mb-md-0">
        {% include figure.liquid loading="eager" path="assets/img/publication_preview/al_stl.gif" title="reward modeling" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    Left: Reward modeling and prediction via Gaussian processes and deep neural networks. Right: Extracted specification-consistent behaviors in simulations, including Nvidia Isaac.
</div>

##### _Modeling and control synthesis for long-horizon tasks using Temporal Behavior Trees_

This work addresses the limitations of long-horizon, myopic reinforcement learning by combining the adaptability of Behavior Trees (BTs) with the formal rigor of temporal logics. While temporal logics enable precise task specification, they struggle with complex dependencies. BTs offer modularity and flexibility but lack formal guarantees. By translating BTs into Timed Automata, this approach enables formal verification, inconsistency detection, and control synthesis using UPPAAL, ensuring robust, time-aware task execution.

###### **References**

- {% reference bt2automata %}
- {% reference omtbt %}

##### _Learning reward functions and control policies that satisfy temporal-logic specifications_

Designing effective reward functions in reinforcement learning (RL) is challenging and error-prone, often leading to unsafe behaviors. This work presents a neurosymbolic learning-from-demonstrations (LfD) framework that leverages Signal Temporal Logic (STL) and user demonstrations to derive temporal reward functions and control policies. Unlike traditional inverse RL, this approach captures non-Markovian rewards and enhances safety and performance. Initially developed for discrete environments, the framework was later extended to continuous and stochastic settings using Gaussian Processes and neural networks.

###### **References**

- {% reference PDN23 %}
- {% reference PDN21 %}
- {% reference PDN20 %}

##### _Learning to improve/extrapolate beyond demonstrator performance_

Machine learning performance relies heavily on data quality and quantity, making noisy or limited demonstrations a challenge in robotics. This work proposes neuro-symbolic apprenticeship learning, using temporal logic-guided reinforcement learning to enable robots to self-monitor and adapt for improved safety and performance. The capabilities of the framework are exhibited on a variety of mobile navigation, fixed-base manipulation and mobile-manipulation tasks using the **Nvidia Isaac** simulator. This paper is published in the proceedings of IROS 2024. Additional details can be found on the [supplemental document](https://aniruddh-puranic.info/assets/pdf/alstl_supp.pdf).

###### **References**

- {% reference PDN_ALSTL %}
- {% reference PDN23 %}

#### **INTERPRETABLE/EXPLAINABLE AI (xAI)**

---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/publication_preview/peglearn_graphs.jpg" title="reward modeling" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/publication_preview/peglearn_rewards.jpg" title="reward modeling" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/publication_preview/mining_stl.jpg" title="reward modeling" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    Left: Generating graphs that explain demonstrator performance and formal specification conflicts. Center: Neural reward modeling from inferred graphs. Right: Mining formal specifications from time-series data.
</div>

##### _Generating explainable temporal logic graphs from human data_

Evaluating human demonstrations is key to learning safe, effective robot policies. Prior LfD-STL methods required manual ranking of STL specifications, represented as a DAG. To reduce this burden, we introduce Performance Graph Learning (PeGLearn), which automatically infers the DAG from demonstrations. PeGLearn enhances explainability, validated via a CARLA driving study, and models surgeon behavior using human feedback in a surgical domain.Additional details can be found on the [supplemental document](https://aniruddh-puranic.info/assets/pdf/peglearn_supp.pdf).

##### _Learning (mining) specifications from temporal data_

Autonomous cyber-physical systems such as self-driving cars, unmanned aerial vehicles, general purpose robots, and medical devices can often be modeled as a system consisting of heterogeneous components. Understanding the high-level behavior of such components, especially equipped with deep learning, at an abstract, behavioral level is thus a significant challenge. Our work seeks to answer: _Given a requirement on the system output behaviors, what are the assumptions on the model environment, i.e., inputs to the model, that guarantee that the corresponding output traces satisfy the output requirement?_ We develop techniques involving decision-tree classifiers, counterexample-guided learning, optimization, enumeration and parameter mining to extract STL specifications that explain system behaviors.

###### **References**

- {% reference PDN23 %}
- {% reference HSCC20 %}
- {% reference ICCPS20 %}

#### **COMPUTER VISION**

---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/publication_preview/tqtl.jpg" title="reward modeling" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/publication_preview/keck_2019.jpg" title="reward modeling" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    Left: Generating graphs that explain demonstrator performance and formal specification conflicts. Center: Neural reward modeling from inferred graphs. Right: Mining formal specifications from time-series data.
</div>

##### _Evaluating the quality of vision-based perception algorithms_

Computer vision is vital for cyber-physical systems, but ensuring the robustness of deep learning-based perception is challenging. Traditional testing relies on ground truth labels, which are labor-intensive to obtain. This work introduces Timed Quality Temporal Logic (TQTL) to formally specify spatio-temporal properties of perception algorithms, enabling evaluation without ground truth.

##### _Vision-based metric for evaluating surgeon's performance_

Due to the lack of instrument force feedback during robot-assisted surgery, tissue-handling technique is an important aspect of surgical performance to assess. We develop a vision-based machine learning algorithm for object detection and distance prediction to measure needle entry point deviation in tissue during robotic suturing as a proxy for tissue trauma.

###### **References**

- {% reference DATE19 %}
- {% reference KECK19 %}
