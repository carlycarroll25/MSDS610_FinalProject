# Flood Detection using Deep Learning

## Overview
This project classifies aerial images as **flooded** or **non-flooded** using deep learning on the FloodNet dataset. The goal is to support fast post-disaster assessment from UAV imagery.

## Data
- FloodNet-Supervised v1.0  
- 2,343 images (train: 1,445, validation: 450, test: 448)
- Segmentation masks converted to binary labels (flood vs non-flood)

## Approach
- Preprocessing: resize (512×512), normalize, mask → binary label  
- Models: **ResNet50** and **ResNet101** (transfer learning)  
- Training: frozen backbone → partial fine-tuning  
- Loss: Binary Cross-Entropy  
- Optimizer: Adam  

## Results
- Both models achieved ~**99.5% accuracy**  
- F1 ≈ **0.98**  
- Similar performance → deeper model did not improve results  

## Key Insight
More complex models don’t always perform better - **ResNet50 was sufficient** for this task.

## Notes
- Dataset is imbalanced  
- Possible scene-level similarity across splits  
- Results should be interpreted cautiously  

## Authors
Carly Carroll, Carissa Rego, Simon Salaj
