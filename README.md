# -YOLOv8-DeepSORT-Object-Tracking

## This repo is for Learning purpose

DeepSORT is a popular tracking algorithm that combines object detection, Kalman filtering, and deep appearance descriptors for single object tracking. In this README, the key components of DeepSORT are discussed.

## Components of DeepSORT
DeepSORT involves several key components and steps to track objects in a video sequence:

YOLOv8 (You Only Look Once version 8) Detection:

YOLOv8 is used for object detection. It provides bounding boxes around objects in each frame of the video.
The output from YOLOv8 contains the coordinates of these bounding boxes.
Difference Vector:

DeepSORT computes a difference vector for each detected object between consecutive frames.
This difference vector helps in associating the same object across frames.
Kalman Filter Prediction:

Kalman filters are used to predict the future location of each tracked object based on its previous motion.
The Kalman filter helps in estimating object position and velocity.
DeepSORT:

The core of DeepSORT integrates object detection with the Kalman filter for object tracking.
It associates detected objects with previously tracked objects and predicts their future positions.
Mahalanobis Distance and Deep Appearance Descriptor:

Mahalanobis distance is used to measure the dissimilarity between detected objects and tracked objects.
Deep appearance descriptors are used to represent the visual appearance of objects.
These descriptors help in matching detected objects with tracked objects.
Hungarian Assignment:

The Hungarian algorithm is used to associate detected objects with tracked objects based on the Mahalanobis distance.
It optimally matches objects in a way that minimizes the overall distance.
Usage
To use DeepSORT, you typically need to set up the YOLOv8 model for object detection, implement the Kalman filter for object prediction, and integrate the Mahalanobis distance calculation and deep appearance descriptors for object matching. You can find open-source implementations of DeepSORT in various programming languages that you can adapt to your specific project.


This notebook is inspired from Muhammad Moin Faisal.
