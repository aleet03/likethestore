---
layout: page
title: projects
permalink: /projects/
description: Selected research and engineering work in robotics, machine learning, and autonomy.
nav: true
nav_order: 1
---

### Robust visual localization

**Mach Industries - 2026-present**

Research and development on visual localization under temporal and other long-tail covariate shifts. My work includes targeted data curation, synthetic data generation, hard-example mining, and fine-tuning and evaluation of SuperPoint/LightGlue models on flight and map-tile imagery.

I built pipelines that reproject flight imagery onto terrain-aware ground planes, generate augmented image pairs, and produce metadata-rich manifests and matching-quality analytics. I also developed model-delivery workflows for PyTorch, ONNX, and TensorRT, with versioned artifacts for edge deployment.

### Trustworthy robotic foundation models

**Trustworthy Robotics Lab, Georgia Tech - 2026-present**

Research on mechanistic interpretability and steerability of Vision-Language-Action models, including representation-preserving fine-tuning for robust and controllable World-Action Models and VLAs under visual perturbation.

### Navigation, estimation, and flight control

**Mach Industries - Summers 2025 & 2026**

Developed high-fidelity simulation and Monte Carlo infrastructure for high-altitude balloon analysis. Implemented an extended Kalman filter with tightly coupled GNSS and barometric measurements, and a physics-informed linear regression correction for GNSS-denied altitude estimation.

For fixed-wing aircraft, I worked on system identification with multisine excitation and implemented LQR and open state-space control in a custom PX4 module.

### Multi-agent autonomous racing

**Dynamics and Control Systems Laboratory, Georgia Tech - 2024-2025**

Researched stochastic planning and control for dynamic multi-agent racing, including adversarial inverse reinforcement learning for reward design. Built a car-merging simulator using an iLQGame solver and benchmarked constrained optimizers for nonlinear generalized Nash equilibrium problems.

I also implemented real-time particle-filter localization and built a low-cost IoT racecar testbed using time-of-flight LiDAR sensors.

### Autonomous aircraft integration

**GT Design-Build-Fly SAE Advanced Class - 2022-2025**

Led controls, software, and avionics development for an international aircraft engineering competition. Integrated COTS avionics on a tri-tiltrotor package-delivery quadplane, tuned VTOL PID gains using flight-log data, and implemented centimeter-level navigation with RTK D-GNSS.
