---
title: "Two-Fingers In-Hand Manipulation"
excerpt: "Tokyo Metropolitan University (<a href='https://sites.google.com/site/ntlabsite/'>Takesue Lab.</a> Aug 2021 - Mar 2023)<br/>Summary: Master's Thesis<br/><img src='/images/project_two-fingers.gif' width='75%'>"
collection: projects
---

<h2>Summary</h2>

This master's thesis develops a two-finger robot hand for in-hand rotation of uncommon-shaped objects with uneven surfaces. In-hand rotation changes an object's orientation within the grasp, reducing the need for complex manipulator trajectories in pick-and-place tasks. Pressure sensors estimate the center of pressure of each finger to assess grasp conditions and guide two proposed approaches: Object On-the-Fly Adjustment (OOA) and Re-grasp Object Movement (ROM).

<figure>
	<img src='/images/project_two-fingers.gif' alt='Two-finger robot hand mounted on the Cobotta robot.' />
	<figcaption>Two-finger robot hand mounted on the Cobotta robot.</figcaption>
</figure>

<h2>System Overview</h2>

<figure>
	<img src='/images/project_two-fingers-system-overview.png' alt='System overview of the two-finger robot and its ROS control system.' />
	<figcaption>System overview of the robot, sensors, controllers, and ROS-based software.</figcaption>
</figure>

<h2>Hand and Finger Design</h2>

<figure>
	<img src='/images/project_two-fingers-hand-design.png' alt='Hand design and joint configuration of the two-finger robot.' />
	<figcaption>Hand design and joint configuration.</figcaption>
</figure>

<figure>
	<img src='/images/project_two-fingers-finger-design.png' alt='Finger design with pressure sensors, fingertip components, and center-of-pressure visualization.' />
	<figcaption>Finger design, pressure sensors, and center-of-pressure visualization.</figcaption>
</figure>

<figure>
	<img src='/images/project_two-finger-finger-design.gif' alt='Animated CAD view of the two-finger robot hand design.' />
	<figcaption>Animated CAD view of the finger mechanism.</figcaption>
</figure>

<h2>Robot Movement</h2>

<figure>
	<img src='/images/project_two-finger-movement.gif' alt='Two-finger robot performing an in-hand manipulation movement.' />
	<figcaption>In-hand manipulation experiment.</figcaption>
</figure>

<h2>Contribution</h2>
* Designed and developed a two-finger gripper with actuated fingertip joints and pressure sensing for manipulating uncommon-shaped objects.
* Proposed two manipulation algorithms, Object On-the-Fly Adjustment (OOA) and Re-grasp Object Movement (ROM), for picking, rotating, and placing objects during in-hand manipulation.
* Evaluated the proposed methods on the robot. ROM achieved an average success ratio of 0.93 (93%), compared with 0.70 for OOA and 0.63 without additional movement.
* Created a visualization in RViz and a simulation in Gazebo to analyze the manipulation process and compare the proposed approaches.

<b>Ulitized:</b> Linux, C/C++, Python, Arduino, ROS, RViz, Gazebo, Cobotta, Dynamixel, Git, Fusion 360

<!-- <b>More Info:</b> [EROS Research Team](http://anhar.lecturer.pens.ac.id/projects/eros/) -->