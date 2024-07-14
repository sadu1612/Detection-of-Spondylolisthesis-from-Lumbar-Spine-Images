# Detection-of-Spondylolisthesis-from-Lumbar-Spine-Images
Dataset used in this project is BUU-LSPINE dataset. - https://services.informatics.buu.ac.th/spine/

The Burapha Spine Dataset version 0.1 are labeled LSPINE X-ray image dataset. The dataset consists of 400 pairs of images with various resolutions sizes. 1 pair of images include AP view (Anterior view) and LA view (Lateral view). Each image was labeled each of the edge of the lumbar spines and diagnosis with 4 spine disorders which include Anterolisthesis, Retrolisthesis Left Laterolisthesis, and Right Laterolisthesis. The diagnosis was done by the physicians. All the LA view images in this dataset are left lateral view (patient look to the left side of the image) and all of the right lateral view images (patient look to the right side of the image) are flipped to left lateral view.


Initially, Lumbar Spine was detected using models YOLOv5, MobileNetV1, ResNet50V1 and EfficientDetD1.
YOLOV5 takes input in text format while remaining models take input in the form of xml files.
Out of all these models, I have achived a maximum precision value of 94.01% and maximum recall of 92.38%.

For Keypoints extraction, I have used YOLOv7 pose model which takes input as text file. Achieved a keypoint loss of 0.0213 and keypoint visibility loss of 0.00042.

For Spondylolisthesis prediction, the initial dataset is made into patches using ground truth annotations. Later, using Spondylolisthesis annotations, predictions were made, achieved a maximum accuracy of 97.90% for SVM model.

For the integrated model, keypoints were first extracted using a keypoints detection model. These keypoints were then used to create patches, which were subsequently input into the spondylolisthesis prediction model.
