---
title: "Research"
layout: default
excerpt: "OpenDIM Lab research directions"
sitemap: false
permalink: /research/
---

# Research

OpenDIM Lab studies how robots can sense, learn, and act in the physical
world. Our research combines tactile sensing, multimodal perception, robot
learning, and dexterous manipulation to develop machines that can interact
with objects reliably and precisely.

<img src="{{ '/images/research-directions.png' | relative_url }}"
     alt="Sense: multimodal sensing and perception; Learn: simulation and robot learning; Act: dexterous robotic manipulation."
     style="display: block; width: 100%; height: auto; margin: 24px auto;">

We focus on three closely connected research directions:

## Tactile sensing and perception

We develop vision-based tactile sensors and learning-based perception methods
for understanding contact, geometry, material properties, and motion. Tactile
observations provide information that is often unavailable to cameras alone,
especially when objects are occluded or when successful manipulation depends
on subtle contact changes.

Our work explores tactile representations, contact localization, surface
reconstruction, tactile motion estimation, and multimodal fusion. By combining
touch with vision, proprioception, and other sensory signals, we aim to give
robots a more complete understanding of their physical interactions and enable
robust perception under changing lighting, viewpoints, and contact conditions.

## Simulation and robot learning

We build scalable tactile simulation and sim-to-real learning methods that
transfer robot skills from virtual environments to the real world. Simulation
enables large-scale data generation, controlled experimentation, and systematic
evaluation of sensing and control strategies that would be expensive or slow
to collect entirely on physical robots.

Our research investigates differentiable and data-driven tactile simulation,
reinforcement learning, imitation learning, and multimodal policy learning.
We design training pipelines that reduce the gap between simulated and real
tactile observations, allowing robots to learn useful behaviors with less
physical data and improved generalization to new objects, surfaces, and
interaction conditions.

## Dexterous robotic manipulation

We develop touch-guided skills for in-hand manipulation, bimanual
coordination, and precise contact-rich tasks. These tasks require robots to
continuously reason about contact forces, object motion, hand configuration,
and uncertainty while coordinating many degrees of freedom.

Our goal is to create manipulation policies that are both capable and
reliable, including skills for grasp adjustment, object rotation, tactile
servoing, pushing, reorientation, and tool-like interaction. By integrating
tactile feedback with learned models and closed-loop control, we seek to
enable dexterous robots to adapt their actions online rather than relying
only on precomputed trajectories or precise object models.
