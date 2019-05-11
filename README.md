# YOLO_for_face_detection

There are different approaches for object detection like sliding windows approach, region proposal methods and single shot detectors. YOLO (You only Look Once) is one of the single shot detector models.

The Object detection problem is reframed into a single regression problem in YOLO, straight from image to box coordinates and class probabilities. A single CNN simultaneously predicts multiple bounding boxes and class probabilities for those boxes. Unlike region proposal and sliding window method, YOLO reasons globally about the image when making predictions.
Since YOLO doesn’t have a complex pipeline, it is extremely fast.

DATA: WIDERFACE dataset, It consists of totally 32,203 images with 393,703 labelled faces.
	Link: http://shuoyang1213.me/WIDERFACE/

The WIDERFACE dataset was preprocessed and then the YOLO network pretrained on COCO dataset is downloaded and the final layers of the network are modified. The network was modified based on the YOLO model in YAD2K (Yet another Darknet 2 Keras) repository. Since the GPU space is less, and due to large number of images, the inputs to the network were converted into generators which keeps only one batch of images in the memory at a time. The model was trained for 42 epochs and each epoch took around 25 minutes to complete.


![alt text](https://raw.githubusercontent.com/jayaramanjay97/YOLO_for_face_detection/master/image_1.png)
![alt text](https://raw.githubusercontent.com/jayaramanjay97/YOLO_for_face_detection/master/image_2.png)
