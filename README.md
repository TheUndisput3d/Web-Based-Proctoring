
# Web Based Proctoring
This Web-Based Proctoring System aims to provide a robust solution for remote exam monitoring using advanced computer vision and machine learning techniques. This system integrates multiple features to ensure the integrity of online assessments by analyzing various
behavioral cues of test-takers.
 
Key components includes: 
     
     1.  Head Pose estimation
     2.  Object Detection
     3.  Face Verification
     4.  Mouth Movement Analysis
     5.  Gaze Tracking
     6.  Face Spoofing

### Head Pose Estimation

The model for Head Pose Estimation Was Created from the Scratch.


The **Pandora dataset** was used  for the head posture module’s training and validation. There
are 100 annotated sequences in the collection, gathered from 10 male and 10 female patients.Every participant gets five recordings. Regarding every topic,Two sequences with
limited mobility are executed.adjusting the roll, pitch, and yaw angles independently.

![Image](https://github.com/user-attachments/assets/a6ef3712-1586-44d3-9434-fd9a67cff44f)

The **BIWI benchmark** dataset was utilized to test the head pose module. It
has fifteen thousand frames, with depth maps (640 × 480) and RGB (640 × 480). Twenty
participants have been participated in the recordings: four of them were double-recorded,
for twenty-four scenes in all. The actual values of pitch, yaw, and Along with the head center and the roll angles, the matrix of calibration.

![Image](https://github.com/user-attachments/assets/e4a46357-75f1-4509-9789-e1728e2ef379)

### Object Detection
OpenCV’s YOLOv7 object detector to identify instances of banned items such as mobile phones, laptops, TVs, and books.
![Image](https://github.com/user-attachments/assets/5f033646-dd9c-4340-80c8-d810f1496de9)

![Image](https://github.com/user-attachments/assets/5f54e6bb-80ea-4ee7-b1e2-208e6e118fdf)




### Face Verification
For Face Verification  Dlib’s face verification model was used to identify the examinee by name. The model
leverages a pre-trained ResNet50 CNN to generate a 128-dimensional feature vector for each
facial image in the database.


![Image](https://github.com/user-attachments/assets/23444be8-d81e-4d34-8482-0a9fb8647b53)

### Face Spoofing
To determine if an examinee is real or using a photograph, a face spoofing detection function
ality was implemented. The process begins by capturing the examinee’s face image through
 the Face Detection module. This image is then converted into YCrCb and CIE Luv* color
 spaces using OpenCV. Histograms are computed for both color spaces and concatenated.
 The concatenated histogram is then fed into Scikit-learn’s ExtraTreesClassifier model to
 classify the face as either real or spoof.

![Image](https://github.com/user-attachments/assets/171c5095-0789-4786-9d81-cd2fe6ec6dff)


![Image](https://github.com/user-attachments/assets/7aa88a14-381d-43ec-9a01-ed54e913f245)

 ### Gaze Tracking
Dlib’s pre-trained network was used  to detect and predict 68 facial landmarks on the user’s face. 
![Image](https://github.com/user-attachments/assets/52d5e41b-69c0-49e6-9070-a60523b1626d)

![Image](https://github.com/user-attachments/assets/c2805117-5bc7-4659-ae5c-ad7741acde42)

### Mouth Movement Analysis
 The lip region is identified using landmarks 60 through 67. To assess whether the mouth is
 open or closed, Lip Aspect Ratio (L.A.R) is defined as:

 L.A.R = |P(62)−P(66)|
 |P(60) − P(64)|

 where P(i) denotes the position of landmark i.
 Through extensive testing, threshold is fixed to 0.1. If the L.A.R exceeds 0.1, it indicates
 that the mouth is open; otherwise, it is considered closed. Additionally, to determine if the
 user is speaking, a buffer mechanism is employed. If the mouth remains open for more than
 10 consecutive frames, it is classified as speaking,

 ![Image](https://github.com/user-attachments/assets/8df4031a-1cbd-41c0-9697-8db34d0f82ad)

![Image](https://github.com/user-attachments/assets/69797a80-eb1d-4bb1-8c28-d7db81f30e02)

### Overall Proctored System
 ![Image](https://github.com/user-attachments/assets/0ba9fbff-71cc-4ec2-9ec5-4b09b56dfba9)

### Web Proctoring on real time examination
![Image](https://github.com/user-attachments/assets/a5222dd2-c5a3-4e2e-a2bc-134502002410)