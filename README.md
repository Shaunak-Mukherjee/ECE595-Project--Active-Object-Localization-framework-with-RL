 ECE595-Project — Active Object Localization Framework with Deep Reinforcement Learning - Reimplementation and Extension

# Active Object Localization with Deep Reinforcement Learning  
### ECE 595 Final Project – Purdue University

This project implements an **active object localization framework** using **Deep Q-Learning**, inspired by Caicedo & Lazebnik (ICCV 2015).  
The agent learns to iteratively refine a bounding box over bird images from the original "Pascal VOC 2007" and "CUB-200-2011" dataset.

---

## Overview

- Custom Gym-style environment (`ActiveEnv`) for dynamic bounding-box manipulation  
- ResNet-50 feature extractor + DQN agent
- Sequential decision-making to localize subjects of interest in images from initial bounding box  
- Evaluation on dataset with IoU metrics and trigger-based accuracy  
- Visualization tools: episode rollouts, heatmaps, bounding-box overlays

---

## Key Features

- Discrete action space (move, scale, aspect-ratio, trigger)  
- Reward shaping based on IoU improvement  
- Episode-level and dataset-level attention heatmaps  
- GIF/MP4 generation for localization trajectories  
- Modular utilities for dataset loading, evaluation, and visualization  

---
### Qualitative Output
<img src="Figure3.svg" width="700px">


---

## How to Run

1. Open the provided Jupyter notebooks in Google Colab and simply 'Run all cells'
2. Mount the CUB dataset and run setup cells  
3. Train the DQN agent  
4. Evaluate using built-in visualization and metric functions  



---

## Contributors

Shaunak Mukherjee  
Grayson Wills  
Christian Okreghe  
Aravind Muraleedharan  
Purdue University – ECE 595
