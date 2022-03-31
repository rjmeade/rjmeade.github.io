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

In 2021, I was part of a senior design project team whose objective was to design, manufacture, and test an autonomous fixed-wing aircraft. The goal was to design a modular fixed-wing test bed that flies for 10 minutes carrying 1 pound of payload. UAV Forge would use the plane as a proof of concept for a fixed-wing design and for developmental testing. My roles on the team were structural design of the wing mount, CADing the plane assembly, and fabrication.

### **Wing Mount Design**
The aircraft wings were manufactured separately from the fuselage to make the aircraft modular and transportable. An attachment mechanism needed to be designed that allowed for quick assembly while being rigid enough for flight. A clamping mount was chosen so that the wing's position along the fuselage could be changed.

<figure>
    <img class="img-responsive" src="/assets/img/wing_attachment_isometric_view.png" alt="" style="display:block;float:none;margin-left:auto;margin-right:auto" />
    <figcaption style="text-align:center"><i>CAD Assembly of Wing Attachment + Carbon Fiber Fuselage</i></figcaption>
</figure>

Since there were strict schedule restrictions and the geometry of the wing-attachment mechanism was fairly complex, we decided to 3D print the part. We chose ABS plastic as the material due to its rigidity and availability.

<figure>
    <img class="img-responsive" src="/assets/img/wing_attachment_side_view.png" alt="" style="display:block;float:none;margin-left:auto;margin-right:auto" />
    <figcaption style="text-align:center"><i>Wing Attachment Side View</i></figcaption>
</figure>

Tensioning was utilized to fix the wing to the wing-attachment mechanism. In the figure above, the orange color represents rubber bands that tension the wing to the fuselage. This strategy allows for convenient assembly and will act as a point of failure in a crash so that the wings do not absorb all of the force. <a href="https://docs.google.com/spreadsheets/d/1OqkLYJSMPUrWA_bF9hzqquYfCP3xtj78jg7_b-HxPtc/edit?usp=sharing" target="_blank">Moment estimations</a> were conducted on the circular struts that protrude from the part to ensure they would not break from tension forces.


##### **Topology Optimization Study**
One of the primary goals of the structural design was to reduce the aircraft's weight. After obtaining an estimate of the forces the wing-attachment mechanism would endure in a crash and in flight, a topology optimization study was conducted to analyze areas where we can cut material without sacrificing structural integrity.

<figure>
    <img class="img-responsive" src="/assets/img/wing_attachment_topology_results.png" alt="" style="display:block;float:none;margin-left:auto;margin-right:auto" />
    <figcaption style="text-align:center"><i>Topology Optimization Results</i></figcaption>
</figure>

We superimposed the optimization results onto our initial model of the Solidworks part and manually cut away unnecessary structure. Ultimately, we were able to reduce the weight of this part by 15% while maintaining a factor of safety of two.

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

##### **Static Load Simulations**
After the topology optimization simulations were conducted, static load simulations were run on the part to ensure it would withstand a crash. Back of the napkin calculations were done to produce a max force value that the aircraft would experience in a crash. The momentum-impulse equation was used to estimate the force, which we applied to a static load simulation in two different scenarios. One where the force is concentrated on the circular struts, and one where the force is concentrated where our carbon fiber wing spars would intersect with the part.

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

We determined that in either case, the maximum stress experienced by the part would be significantly less than the 20 MPa maximum stress threshold of 40% infill ABS \[1\]. We 3D-printed the design and used it on the final iteration of the aircraft.

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