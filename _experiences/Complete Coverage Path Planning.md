---
layout: experience
title: "Complete Coverage Path Planning"
categories: misc
location: "University of California, Irvine"
priority: "3"
excerpt: "Analytical solution for complete coverage path planning in concave regions."
---

<figure>
    <img class="img-responsive" src="/assets/img/2021_bcd_2.png" alt="" style="display:block;float:none;margin-left:auto;margin-right:auto" />
    <figcaption style="text-align:center"><i>Boustrophedon Decomposition Software Output</i></figcaption>
</figure>

One of my primary responsibilities on UAV Forge last year was to design and implement our drone's path planning algorithm. We were tasked with searching a region for targets in the most time-efficient manner possible due to strict flight time restrictions, an archetype of problem called complete coverage path planning.

Complete coverage path planning is the process of generating a path for our drone to follow that allows it to visit every point in a specified area. Since the competition does not provide the exact geographic location of each target, the drone must cover every point in the search area. Below is a figure showing an example of a complete coverage path.

<figure>
    <img class="img-responsive" src="/assets/img/path_planning_example.png" alt="" style="display:block;float:none;margin-left:auto;margin-right:auto" />
    <figcaption style="text-align:center"><i>Complete Coverage Example [1]</i></figcaption>
</figure>

### **Boustrophedon Decomposition**

Our approach utilizes a method called boustrophedon cell decomposition, which first divides the search area into individual subregions. The path planning algorithm then sweeps each subregion individually. Boustrophedon decomposition is deterministic and 

<figure>
    <img class="img-responsive" src="/assets/img/sample_mission_map.png" alt="" style="display:block;float:none;margin-left:auto;margin-right:auto" />
    <figcaption style="text-align:center"><i>Sample Mission Map</i></figcaption>
</figure>

##### **Computing Convex and Concave Vertices**
concave vs convex, computing cross product

##### **Optimal Sweep Angle**
angle changing for optimal sweep angle

##### **Sweeping Subregions**
lawnmower pattern

##### **References**
\[1\]  E. Horváth, C. Pozna, and R. Precup, "Robot Coverage Path Planning Based on Iterative Structured Orientation," <i>Acta Polytechnica Hungarica</i>, vol. 15, no. 2, 2018.
