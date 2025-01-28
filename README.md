# Human_pose_pro
human_pose_detection
Human pose estimation from video plays a critical role in various applications such as quantifying physical exercises, sign language recognition, and full-body gesture control. For example, it can form the basis for yoga, dance, and fitness applications. It can also enable the overlay of digital content and information on top of the physical world in augmented reality.


An example of a graphical skeleton is shown below:
![pic](https://github.com/user-attachments/assets/43ade5f5-fe95-4c90-92d1-17864d5ded9b)

So how does it work?
MediaPipe uses TensorFlow lite in the backend. Using a detector first locates the person (ROI) within the frame. Then it uses the ROI cropped frame as INPUT and predicts the landmarks/key-points within the ROI. The mediaPipe pose estimator detects a total of 33 key points.

MediaPipe pose estimation is a single 3D pose estimator. It detects x, y, and z coordinates for each landmark. Z-axis is basically information about the depth of a landmark. That means how far or close the landmarks are from the camera relative to the other landmarks.

MediaPipe Pose is a ML solution for high-fidelity body pose tracking, inferring 33 3D landmarks and background segmentation mask on the whole body from RGB video frames utilizing our BlazePose research that also powers the ML Kit Pose Detection API. Current state-of-the-art approaches rely primarily on powerful desktop environments for inference, whereas our method achieves real-time performance on most modern mobile phones, desktops/laptops, in python and even on the web.

![pic1](https://github.com/user-attachments/assets/4b3bcd54-f4e8-42ca-95fa-353f4ae42f73)
MediaPipe Pose real-world 3D coordinates
Pose Estimation Quality
To evaluate the quality of our models against other well-performing publicly available solutions, we use three different validation datasets, representing different verticals: Yoga, Dance and HIIT. Each image contains only a single person located 2-4 meters from the camera. To be consistent with other solutions, we perform evaluation only for 17 keypoints
![image](https://github.com/user-attachments/assets/49bbf26f-18bb-46c8-8a37-c3ebf60487b7)

Categories of human pose detection:
2D pose estimation: In 2d pose estimation only the x and y coordinates are predicted for each landmark in an image. It doesn’t give any information about the skeleton’s angles or the rotation or orientation of an object or human instance.

3D pose estimation: 3d pose estimation allows us to predict the spiral position of a human. It gives x, y, and z coordinates for each landmark. With 3d pose estimation, we can determine the angle of each joint of a human skeleton.

Rigid pose estimation: Rigid pose estimation is also known as 6D pose estimation. It provides all information about the human pose as well as the rotation and orientation of a human instance.

Single pose estimation: In a single pose estimation model only one human’s pose can be predicted in an image.

Multi pose estimation: In multi-pose estimation, Multiple human poses can be predicted in an image at the same time.

Human Pose detection with OpenCV Output:
![image](https://github.com/user-attachments/assets/3c20e84b-4523-4223-ba51-d5a9d4158383)





