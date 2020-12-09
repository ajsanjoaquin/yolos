# YOLO v3 Pytorch Implementation

I followed (Ayoosh Kathuria's tutorial)[https://blog.paperspace.com/how-to-implement-a-yolo-object-detector-in-pytorch/] to understand how the YOLO Algorithm works.

## YOLO v3
The YOLO class of algorithms seek to detect objects, draw bounding boxes around them, and label them with their corresponding classes in real-time. YOLO v3 uses Darknet-106 for object detection, which makes it slower (<=30 FPS) but more accurate than YOLO v2. One major improvement of v3 is that it makes detections at three different scales, which makes it ideal for detecting small objects in real-time.

## Files

**darknet.py** - Code for Darknet-106 </br>
**detector.py** - Code for YOLO algorithm </br>
**dog-cycle-car.png** - sample image to test the model. det folder also includes its predicted version </br>

Download the official pre-trained weights (here)[https://pjreddie.com/media/files/yolov3.weights]