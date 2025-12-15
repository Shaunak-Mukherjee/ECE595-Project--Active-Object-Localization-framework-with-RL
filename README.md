# ECE595-Project — Active Object Localization Framework with Deep Reinforcement Learning  
**Reimplementation and Extension**

## Active Object Localization with Deep Reinforcement Learning  
**ECE 595 Final Project – Purdue University**

This project implements an **active object localization framework** using **Deep Q-Learning**, inspired by *Caicedo & Lazebnik, “Active Object Localization with Deep Reinforcement Learning” (ICCV 2015)*.

The initial phase of the project uses **Pascal VOC 2007** primarily as a **verification dataset** to ensure that the reinforcement learning agent, action space, and bounding-box refinement logic function correctly in a standard object detection setting. Once correctness and stability were validated, the framework was **extended to the CUB-200-2011 bird dataset**, a simpler and more controlled domain, to clearly demonstrate the agent’s ability to localize a single dominant object through sequential decision-making.

---

## Contributors
- Shaunak Mukherjee  
- Grayson Wills  
- Christian Okreghe  
- Aravind Muraleedharan  

**Purdue University — ECE 595 (Artificial Intelligence)**

---

## Overview
- Custom **Gym-style reinforcement learning environment** for dynamic bounding-box manipulation  
- **ResNet-50 feature extractor** paired with a **Deep Q-Network (DQN)** agent  
- Sequential decision-making process for object localization starting from an initial bounding box  
- Evaluation using **Intersection over Union (IoU)** metrics and trigger-based accuracy  
- Visualization utilities for tracking agent behavior and decision trajectories  

---

## Key Features
- Discrete **action space** including movement, scaling, aspect-ratio adjustment, and trigger actions  
- **Reward shaping** based on incremental IoU improvement  
- Support for **episode-level and dataset-level analysis**  
- Modular utilities for dataset loading, training, evaluation, and visualization  
- Reproducible experiments via clearly structured notebooks  

---

## How to Run
1. Open the provided **Jupyter notebooks** in **Google Colab**
2. 'Reinforcement_Learning_Final_Project_Showcase.ipynb' is reimplementation using Pascal VOC dataet and notebook
   'Final_Run_Reinforcement_Learning_Final_Project_Showcase_CUB_200_2011.ipynb' - extension to CUB-200-2011 dataset 
4. Run all cells in order (datasets and experiments are clearly separated by notebook)  
5. Mount the required dataset (Pascal VOC or CUB-200-2011) when prompted  
6. Execute setup cells to initialize the environment and models  
7. Train the DQN agent  
8. Evaluate performance using built-in metric and visualization functions  
