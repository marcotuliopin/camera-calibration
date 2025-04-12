# Camera Calibration using DLT (Direct Linear Transform)

This repository implements a complete camera calibration pipeline from scratch using the DLT (Direct Linear Transform) method, based on homography estimation and SVD decomposition.

The goal of this project is to perform camera calibration without using OpenCV's automatic functions (`cv2.calibrateCamera`), allowing full control and understanding of the mathematical process involved.

---

## Algorithm Overview

The implemented method follows these main steps:

1. Definition of 3D world points (in millimeters).
2. Manual correspondence of these points with 2D image points (in pixels).
3. Construction of matrix \( A \) for the DLT system \( Ax=0 \).
4. Solving using SVD to obtain the projection matrix \( P \).
5. Extraction of the intrinsic matrix \( K \), rotation matrix \( R \), and camera center \( C \) from \( P \).
6. Visualization of the projected points onto the image for validation.
