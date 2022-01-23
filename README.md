# 6DoF-camera-pose
The aim of this task is to find 6Dof pose of camera in images img2 and img3 w.r.t. pose in reference image img1.

There are 2 different solutions implemented in this work. 

First solution:
1. Initially the camera is calibrated using calibrateCamera function and obtained calibrated cameraMatrix.
2. Then SIFT features are extracted on pair images and keypoints are matched.
3. EssentialMatrix estimated with matched keypoints.
4. Relative pose of camera estimated using recoveryPose with EssentialMatrix.
5. Relative pose scaled and visualized the trajectory.

Alternative solution:
1. Calibrated camera and obtained camera intrinsic matrix.
2. Calculated flow of vr2d points on target image with Lucas-Kanade Optical Flow algorithm.
3. Solved Pnp on target image with projected 2D - 3D correspondences to find the pose.
4. Visualized the trajectory.

<img src="3d_trajectory_try1.jpg" width="200" height="200" />