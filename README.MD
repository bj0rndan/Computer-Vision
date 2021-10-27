# F1 Car Object Detection
This repository is the result of my first attempt on creating an accurate machine learning 
model capable of localizing and identifying F1 Car in a single image. Based on 
[Tensorflow pre-trained on COCO dataset detection model](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf1_detection_zoo.md), but retrained
with a total of 146 images (122 and 26 in train and test set respectivelly). <p align="center">
<img src="https://github.com/bj0rndan/Computer-Vision/blob/main/f1(4).png" width = 1024 height = 576> </p>

## Data Preparation
* The initial images were extracted cropping a video
* Resulting images were randomly distributed between train and test folders
* All images in both train and test folders were manually labeled with the [LabelImg graphical image annotation tool](https://github.com/tzutalin/labelImg), creating an *.XML* file for each image following the *PASCAL VOC* format
* *.XML* files were gathered into two *.CSV* files (separatelly for train and test sets) using the written *xml_to_csv.py* script
* By means of *tf_records.py* script Tensorflow Record files were created for both train and test set 
