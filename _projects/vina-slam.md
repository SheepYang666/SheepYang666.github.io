---
layout: project
title: "VINA-SLAM"
description: "Voxel-based Inertial and Normal-Aligned LiDAR-IMU SLAM"
permalink: /projects/vina-slam
img: assets/img/projects/vina-slam-teaser.png
importance: 1
category: SLAM
keywords: SLAM, LiDAR, IMU, Odometry, Voxel Map
related_publications: false
github: https://github.com/SheepYang666/VINA-SLAM
---

## Overview

**VINA-SLAM** (Voxel-based Inertial and Normal-Aligned LiDAR-IMU SLAM) is a robust LiDAR-Inertial odometry system designed for challenging environments with sparse or repetitive geometric structures, such as long corridors and narrow staircases.

## Key Features

- **Global Voxel Map**: Establishes a unified 3D global voxel map that collects global structural cues
- **Normal-guided Correspondence**: Uses surface normals stored in the global voxel map for continuous tracking
- **Tangent-space Metric**: Explicitly supplements rotation constraints around planar regions in local Bundle Adjustment
- **Minimum Eigenvalue Factor**: Uses the minimum eigenvalue of voxel covariance as a plane factor to improve Hessian conditioning

## Method

The system employs a tightly-coupled LiDAR-IMU framework with:

1. **IMU Preintegration**: High-frequency motion prediction between LiDAR scans
2. **Voxel-based Mapping**: Efficient point cloud organization using octree voxel maps
3. **Sliding Window BA**: Joint optimization with IMU factors, normal consistency factors, and plane constraints
4. **Robust Initialization**: Automatic system initialization in various scenarios

## Supported Sensors

- Livox Mid360
- Robosense
- HILTI LiDAR
- Ouster
- Velodyne
- Hesai

## Results

The system demonstrates robust performance in challenging environments where traditional LiDAR-IMU odometry methods struggle, particularly in:

- Long corridors with limited geometric features
- Narrow staircases with repetitive structures
- Open areas with sparse geometric constraints

## Code

The source code is available on [GitHub](https://github.com/SheepYang666/VINA-SLAM).

## Citation

```bibtex
@article{vinaslam2024,
  title={VINA-SLAM: Voxel-based Inertial and Normal-Aligned LiDAR-IMU SLAM},
  author={Yang, Yang},
  journal={arXiv preprint},
  year={2024}
}
```

## Contact

For questions and discussions, please open an issue on the [GitHub repository](https://github.com/SheepYang666/VINA-SLAM/issues).
