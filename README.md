# pose-estimation-opencv-tf
Pose Estimation assignment using OpenCV (python)

Implementation of pose estimation problem with video input. I used the pre-trained Caffe Model that won the COCO keypoints challenge in 2016 and Multi-person pose estimation model.

This problem requires to detect and localize the major parts/joints of the body ( e.g. shoulders, ankle, knee, wrist, etc.)
The model takes as input a color image of size w × h and produces, as output, the 2D locations of keypoints for each person in the image. The 2 models I implemented use - COCO 18 points and MPII 15 points.

COCO Output Format Nose – 0, Neck – 1, Right Shoulder – 2, Right Elbow – 3, Right Wrist – 4, Left Shoulder – 5, Left Elbow – 6, Left Wrist – 7, Right Hip – 8, Right Knee – 9, Right Ankle – 10, Left Hip – 11, Left Knee – 12, LAnkle – 13, Right Eye – 14, Left Eye – 15, Right Ear – 16, Left Ear – 17, Background – 18 
MPII Output Format Head – 0, Neck – 1, Right Shoulder – 2, Right Elbow – 3, Right Wrist – 4, Left Shoulder – 5, Left Elbow – 6, Left Wrist – 7, Right Hip – 8, Right Knee – 9, Right Ankle – 10, Left Hip – 11, Left Knee – 12, Left Ankle – 13, Chest – 14, Background – 15

Model weights link: https://github.com/CMU-Perceptual-Computing-Lab/openpose/blob/master/models

Steps I took to implement this pipeline:
1. Downloading model weights
2. Loading the network (.prototxt and .caffemodel)
3. Read image and prepare input to the network
4. Make predictions and parse keypoints
5. Draw skeleton

To run this code:
1. Download weights from above link and paste it in "pose/COCO" and "pose/mpi" folders respectively 
2. Inference notebook can be directly run with respective images
3. Run PoseEstVideo.py with sample videos to get the video output
