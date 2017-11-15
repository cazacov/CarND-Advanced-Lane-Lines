## Advanced Lane Finding Project ##

The goals / steps of this project are the following:
1. Compute the camera calibration matrix and distortion coefficients given a set of chessboard images.
2. Apply a distortion correction to raw images.
3. Use color transforms, gradients, etc., to create a thresholded binary image.
4. Apply a perspective transform to rectify binary image ("birds-eye view").
5. Detect lane pixels and fit to find the lane boundary.
6. Determine the curvature of the lane and vehicle position with respect to center.
7. Warp the detected lane boundaries back onto the original image.
8. Output visual display of the lane boundaries and numerical estimation of lane curvature and vehicle position.
9. Genrate video with the pipeline designed above.

The code is stored in Jupyter Notebook named "project.ipynb" and has exactly the same topic numeration.

 ### 1. First, I'll compute the camera calibration using chessboard images ###
 
 Project contains sample images of a chessboard taken with the car camera. OpenCV function findChessboardCorners finds corners and returns them as array. These image points should match reference object points. The grid of object points is generated with numpy function mgrid.
 
 List of ideal object points and the list of real image points captured by camera are then passed to the OpenCV function calibrateCamera that automatically calculates transformation tht should compensate camera lens distortion.
 
 The transformation matrix is stored in Python variable "mtx" for following calculations.
 
 Here is the result of distortion compensation:
 
<img src="./img/undistorted.png" />

           