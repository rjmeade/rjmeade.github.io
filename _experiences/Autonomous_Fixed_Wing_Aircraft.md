---
layout: experience
title: "Autonomous Fixed-Wing Aircraft"
categories: misc
location: "University of California, Irvine"
priority: "5"
excerpt: "Utilized Solidworks Topology Optimization to minimize weight of aircraft components."
---

<figure>
    <img class="img-responsive" src="/assets/img/2021_sdp_fixed_wing_front.jpg" alt="" style="display:block;float:none;margin-left:auto;margin-right:auto" />
    <figcaption style="text-align:center"><i>Fixed-Wing on Test Day</i></figcaption>
</figure>

uci senior design project. requirements (MODULAR fixed-wing test bed that flies for x amount of time and can carry x payload). my role on the team (structural design, CAD, electronics verification, manufacturing and assembly).

### **Wing Mount Design**
manufacturing wings separately from fuselage to make our aircraft modular and transportable, need a way to attach wings to fuselage. wanted something where we could take wings off and replace with new wings in less then a couple mins.

clamping mount to adjust wing positioning along the fuselage and to adjust cog.

<figure>
    <img class="img-responsive" src="/assets/img/wing_attachment_isometric_view.png" alt="" style="display:block;float:none;margin-left:auto;margin-right:auto" />
    <figcaption style="text-align:center"><i>CAD Assembly of Wing Attachment</i></figcaption>
</figure>

decided to 3dp for rapid prototyping, quick changes if necessary and it was a fairly custom part so 3dp good for manufacturing random geometries.

<figure>
    <img class="img-responsive" src="/assets/img/wing_attachment_side_view.png" alt="" style="display:block;float:none;margin-left:auto;margin-right:auto" />
    <figcaption style="text-align:center"><i>Wing Attachment Side View</i></figcaption>
</figure>

used tensioning to secure wing to fuselage (beige color is rubber bands in the figure). convenient for assembly and act as a point of failure so wings do not break in a crash (most labor-intensive part of our assembly).
moment calculations
https://docs.google.com/spreadsheets/d/1OqkLYJSMPUrWA_bF9hzqquYfCP3xtj78jg7_b-HxPtc/edit?usp=sharing

##### **Topology Optimization Study**
wanted to reduce weight as much as possible, was one of our main concerns with our design. wanted to ensure that we are not overdesigning. use solidworks topology optimization to analyze areas where we can cut material out without sacrificing structural integrity.

<figure>
    <img class="img-responsive" src="/assets/img/wing_attachment_topology_results.png" alt="" style="display:block;float:none;margin-left:auto;margin-right:auto" />
    <figcaption style="text-align:center"><i>Topology Optimization Results</i></figcaption>
</figure>

superimposed optimization results onto initial model of the solidworks part and manually cut away unnecessary structure.

<div class="row">
  <div class="column">
    <figure>
    <img class="img-responsive" src="/assets/img/wing_attachment_cad_before.png" alt="" style="display:block;float:none;margin-left:auto;margin-right:auto" width="400" height="248"/>
    <figcaption style="text-align:center"><i>Before</i></figcaption>
    </figure>
  </div>
  <div class="column">
    <figure>
    <img class="img-responsive" src="/assets/img/wing_attachment_cad_After.png" alt="" style="display:block;float:none;margin-left:auto;margin-right:auto" width="400" height="248"/>
    <figcaption style="text-align:center"><i>After</i></figcaption>
    </figure>
  </div>
</div>

reduce weight by 15%


##### **Static Load Simulations**
after weight cut, worried about design withstanding forces.

back of napkin calculations with rough assumptions to generate max force. used moment impulse equation to estimate force plane would experience in worst case scenario (crash). applied force to static load simulation in two scenarios, one where force concentrated on circular struts and one where force concentrated where carbon fiber rod would be

<div class="row">
  <div class="column">
    <figure>
    <img class="img-responsive" src="/assets/img/wing_attachment_load_sim_spar.png" alt="" style="display:block;float:none;margin-left:auto;margin-right:auto" width="437" height="220"/>
    <figcaption style="text-align:center"><i>Spar (Max Stress: 0.24MPa)</i></figcaption>
    </figure>
  </div>
  <div class="column">
    <figure>
    <img class="img-responsive" src="/assets/img/wing_attachment_load_sim_strut.png" alt="" style="display:block;float:none;margin-left:auto;margin-right:auto" width="363" height="220"/>
    <figcaption style="text-align:center"><i>Strut (Max Stress: 5.5MPa)</i></figcaption>
    </figure>
  </div>
</div>

evaluated against PETG (3dp material) 40% infill maximum stress threshold of 20MPa \[1\], both cases had a factor of safety of 3.5+, printed design and used in final iteration of aircraft.

##### **References**

[1] G. Johnson and J. French, “Evaluation of Infill Effect on Mechanical Properties of Consumer 3D Printing Materials,” <i>Advances in Technology Innovation</i>, vol. 3, no. 4, pp. 179-84, July 2018.

<style>

/* Create two equal columns that floats next to each other */
.column {
  float: left;
  width: 45%;
  padding: 10px;

}

/* Clear floats after the columns */
.row:after {
  content: "";
  display: table;
  clear: both;
}

/* Responsive layout - makes the two columns stack on top of each other instead of next to each other */
@media screen and (max-width: 600px) {
  .column {
    width: 100%;
  }
}
</style>