---
layout: experience
title: "UAV Forge"
categories: misc
location: "University of California, Irvine" # Student-led project at the University of California, Irvine
priority: "1"
excerpt: "Chief Engineer for UCI student-led engineering project."
---

<figure>
    <img class="img-responsive" src="/assets/img/2022_hex.jpg" alt="" style="display:block;float:none;margin-left:auto;margin-right:auto" />
    <figcaption style="text-align:center"><i>2022 Competition Season Drone</i></figcaption>
</figure>


UAV Forge is an interdisciplinary engineering competition team at UCI participating in the annual <a href="https://www.auvsi-suas.org" target="_blank">AUVSI-SUAS</a> competition, which simulates an automated aerial vehicle package delivery mission. UAV Forge is tasked with designing, manufacturing, assembling, and testing a drone that autonomously:
- Navigates waypoints
- Maps and identifies targets in a search area
- Actively avoids other drones and obstacles 
- Airdrops an autonomous ground vehicle

As Chief Engineer for the 2021-2022 season, my primary responsibilities on the team are oversight of the engineering design process, including the design, manufacturing, and integration of all software and hardware components, coordination of project scheduling, and the completion of competition deliverables (Technical Design Paper, Design Review Poster).

### **Engineering Design Process**
A core component of UAV Forge is our commitment to a rigorous, objective design process. Each decision we make about individual electrical and structural components will ultimately impact the performance of our final system, so it is imperative that every design decision is made purposefully, thoroughly considering alternative solutions. Throughout the quarter, we introduced design process tools such as decision matrices and trade studies, which members are strongly encouraged to utilize when deciding between designs.

The AUVSI Competition Rules provide tasks and scoring equations, which were developed into system requirements. Marginal and ideal values were determined based on maximizing competition points. System requirements ensure that subteams operate cohesively and allow design teams to cross-reference individual subsystem designs with the goals of the overall system.

<figure>
    <img class="img-responsive" src="/assets/img/system_requirements_color.jpg" alt="" style="display:block;float:none;margin-left:auto;margin-right:auto" />
    <figcaption style="text-align:center"><i>System Requirements Analysis</i></figcaption>
</figure>

In order to justify purchasing and design decisions, numerical analysis is conducted to decide between different designs or components. In the figure below, we used manufacturer data to estimate flight time for two different motor configurations. Graphs of flight time (pictured on the right) indicated that KDE5215XF-330 motors provide greater flight time across all throttle and thrust ranges. Therefore, they were the clear choice to use on the competition vehicle.

<figure>
    <img class="img-responsive" src="/assets/img/flight_time_estimate.png" alt="" style="display:block;float:none;margin-left:auto;margin-right:auto" />
    <figcaption style="text-align:center"><i>Flight Time Estimate</i></figcaption>
</figure>

Competition payload requirements significantly increase the total weight of the drone. The additional loads impose considerable thrust requirements on the drone's motors. A comparison of motor configurations was performed to determine whether increasing propeller size would improve drone performance. In Figure 3 below, our selected motor configuration is shown in black, overlayed on top of performance data derived from long propeller configurations.

<figure>
    <img class="img-responsive" src="/assets/img/motor_comparison_2.jpg" alt="" style="display:block;float:none;margin-left:auto;margin-right:auto" />
    <figcaption style="text-align:center"><i>Thrust vs. Current for Various Motor Configurations</i></figcaption>
</figure>

Though the data indicate that longer propellers would increase the thrust generated per amp of current by approximately 30%, significant changes to the drone's structure would have to be made to accommodate longer propellers. The team determined that the current motor-propeller configuration suits the system requirements, and an alternate configuration was not pursued.

### **Testing**
Throughout the competition season, three levels of testing are applied to each component of the drone to ensure consistent performance:
 - **Unit Test**: Individual component function is verified.
     - Example: Verify that a motor rotates at a specified RPM under predetermined current load.
 - **Integration Test**: Subsystems comprised of multiple components are assembled and tested.
     - Example: Mount multiple motors to the drone frame and conduct a static thrust test.
 - **System Test**: Multiple subsystems are combined to perform high-level functions.
     - Example: Drone autonomously navigates a waypoint mission and lands.

 By following a layered, progressive testing procedure, design conflicts or issues with component integration can be caught early on in the testing process. A system-level testing plan outlines target testing dates for various system tests required by the AUVSI competition. Results from these tests are documented and submitted with the team's flight readiness review in June.

<figure>
    <img class="img-responsive" src="/assets/img/testing_schedule.jpg" alt="" style="display:block;float:none;margin-left:auto;margin-right:auto" />
    <figcaption style="text-align:center"><i>Testing Schedule</i></figcaption>
</figure>
