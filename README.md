Vehicle Speed Estimation using Optical Flow
Project Overview
This project estimates the speed of moving vehicles in a video using Optical Flow techniques from computer vision. The system analyzes the motion between consecutive video frames to detect moving vehicles and estimate their speed. Bounding boxes are drawn around detected vehicles and their approximate speed is displayed in kilometers per hour (km/h).

The project demonstrates how motion analysis can be used for traffic monitoring, intelligent transportation systems, and surveillance applications.

Objectives :
Detect moving vehicles from a traffic video.
Track motion using optical flow.
Estimate vehicle speed based on pixel displacement.
Display the calculated speed on the video in real time.

Technologies Used :
Python
OpenCV
NumPy
These tools are used for video processing, motion estimation, and mathematical calculations.

Key Concepts Used
Optical Flow
Optical Flow is a computer vision technique used to estimate the motion of objects between two consecutive frames of a video. It calculates the displacement of pixels, which helps determine the direction and speed of moving objects.

In this project, the Farneback Optical Flow algorithm is used to compute dense motion vectors between frames.
Background Subtraction
Background subtraction helps identify moving objects by separating foreground objects from the static background.
This project uses MOG2 Background Subtractor to detect moving vehicles in the scene.

Vehicle Detection
Contours are extracted from the foreground mask to detect potential vehicles. Small contours or irregular shapes are filtered out to reduce noise.

How the System Works
The video is loaded using OpenCV.
Each frame is converted to grayscale.
Optical flow is calculated between consecutive frames.
Background subtraction identifies moving regions.
Contours are extracted to detect vehicles.
Bounding boxes are drawn around detected vehicles.
Speed is estimated based on optical flow magnitude.
The calculated speed is displayed on the video frame.

Speed Estimation Method
Vehicle speed is estimated using the formula:
Speed = Average Optical Flow Magnitude × Scale Factor × FPS

Where:
Optical Flow Magnitude represents pixel displacement.
Scale Factor converts pixels into real-world distance.
FPS represents frames processed per second.
The final speed is converted from meters per second to kilometers per hour (km/h).

Output
The program processes the video and displays:
Detected vehicles with bounding boxes
Estimated vehicle speed in km/h
Real-time visual output of the traffic scene








