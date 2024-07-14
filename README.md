# Detection-of-Spondylolisthesis-from-Lumbar-Spine-Images

Initially, Lumbar Spine was detected using models YOLOv5, MobileNetV1, ResNet50V1 and EfficientDetD1.
YOLOV5 takes input in text format while remaining models take input in the form of xml files.
Out of all these models, I have achived a maximum precision value of 94.01% and maximum recall of 92.38%.

For Keypoints extraction, I have used YOLOv7 pose model which takes input as text file. Achieved a keypoint loss of 0.0213 and keypoint visibility loss of 0.00042.

For Spondylolisthesis prediction, the initial dataset is made into patches using ground truth annotations. Later, using Spondylolisthesis annotations, predictions were made, achieved a maximum accuracy of 97.90% for SVM model.
