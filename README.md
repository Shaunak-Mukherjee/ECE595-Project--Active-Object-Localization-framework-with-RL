 ECE595-Project — Active Object Localization Framework with Deep Reinforcement Learning - Reimplementation and Extension

This repository contains our final project for ECE 595: Reinforcement Learning at Purdue University (Fall 2025).  
We re-implement and extend the method introduced in *“Active Object Localization with Deep Reinforcement Learning”* (Caicedo & Lazebnik, ICCV 2015) and apply it to the fine-grained **CUB-200-2011** bird dataset.

Our framework trains a Deep Q-Network (DQN) agent to iteratively refine a bounding box around a target bird species using a sequence of discrete actions. The agent learns a policy that moves a bounding box through the image until it reaches a satisfactory localization accuracy.

---

## 🔍 Project Overview

Traditional object localization relies on region proposals or exhaustive search.  
In contrast, **Active Object Localization** treats localization as a *sequential decision process*:

- The agent starts with a coarse bounding box.
- It selects actions (move, scale, aspect ratio adjustments).
- After each step, the environment updates the bounding box.
- The episode ends when the agent predicts the **trigger action** (stop) or exceeds max steps.

Rewards are based on improvements in IoU (Intersection over Union) between predicted and ground-truth boxes.

Our implementation includes:

- A custom **CUBActiveEnv** environment following OpenAI Gym API  
- A **ResNet-50** feature extractor for state embeddings  
- A **DQN agent** for sequential localization  
- Evaluation modules, visualization tools, GIF/MP4 generators  
- Attention heatmaps for interpretability

---

## 📁 Repository Structure

