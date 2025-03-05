# Efficient 3D Human Pose Estimation Using Hourglass Tokenizer (HoT)

## Overview 
This project focuses on estimating 3D human poses from 2D monocular video inputs in real-time. The proposed Hourglass Tokenizer (HoT) architecture integrates an Hourglass Network for hierarchical feature extraction and Transformers for capturing global interdependencies. The model is designed to achieve high accuracy with reduced computational cost, making it suitable for real-time applications such as robotics, AR/VR, healthcare, and sports analytics.

## Key Features 
- Hourglass Network for feature extraction
- Transformer Encoder for modeling spatial relationships
- Token Pruning Cluster (TPC) for computational efficiency
- Token Recovering Attention (TRA) for reconstructing full-length features
- Trained on Human3.6M Dataset for robust 3D pose estimation
- Optimized for real-time processing

## Architecture

```
Input: 2D key points extracted using pose detection tools (e.g., OpenPose)
↓
Hourglass Network:
   - Downsampling: Captures large-scale features
   - Upsampling: Recovers fine-grained details
   - Skip Connections: Efficient feature learning
↓
Transformer Encoder: Models spatial relationships
↓
Output: 3D Keypoints (Cartesian Coordinates)
```

## Dataset
We use the Human3.6M dataset, which includes:
- 2D keypoints extracted from annotated video frames
- Ground truth 3D keypoints for supervised learning
- Preprocessing techniques like normalization and data augmentation

## Evaluation
- Mean Per Joint Position Error (MPJPE)
- Visual Comparisons between predicted and ground truth 3D poses

## Future Work
- Enhancing temporal modeling for video sequence predictions
- Optimizing for edge devices to enable real-time applications
- Extending deployment to AR/VR, healthcare, and autonomous systems
