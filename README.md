# YOLO Playground (Exploring different YOLO implementations and deployment)

# YOLO v3 Pytorch Implementation

I followed [Ayoosh Kathuria's tutorial](https://blog.paperspace.com/how-to-implement-a-yolo-object-detector-in-pytorch/) to understand how the YOLO Algorithm works.

## YOLO v3
The YOLO class of algorithms seek to detect objects, draw bounding boxes around them, and label them with their corresponding classes in real-time. YOLO v3 uses Darknet-106 for object detection, which makes it slower (<=30 FPS) but more accurate than YOLO v2. One major improvement of v3 is that it makes detections at three different scales, which makes it ideal for detecting small objects in real-time.

## Files

**darknet.py** - Code for Darknet-106 </br>
**detector.py** - Code for YOLO algorithm </br>
**dog-cycle-car.png** - sample image to test the model. det folder also includes its predicted version </br>

Download the official pre-trained weights [here](https://pjreddie.com/media/files/yolov3.weights)

# YOLO v4 (tiny) for Android (Tensorflow Lite) (Real-time)

It uses the official weights, which was then converted to .tflite. The code is taken from [hunglc007's implementation](https://github.com/hunglc007/tensorflow-yolov4-tflite). It has further improvements from v3 with faster FPS and improved accuracy. I simply followed [Roboflow's tutorial](https://blog.roboflow.com/how-to-train-a-custom-mobile-object-detection-model/).

# YOLO v5 for Android (NCNN) (Static)

It uses the official weights and adapted to Tencent's NCNN framework for Android deployment by [nihui here](https://github.com/nihui/ncnn-android-yolov5). Currently, it only supports images, and I have yet to modify the code. YOLO v5 [purportedly has better accuracy and speed than v4](https://blog.roboflow.com/yolov4-versus-yolov5/).

# To Do
1. Train v4 or v5 on Custom Labels </br>
2. Deploy v5 for real-time detection on Android (Currently facing FPS drops, but [this implementation](https://github.com/zldrobit/yolov5/tree/tf-android) is promising). (Pytorch->ONNX->tflite) </br>
3. Wait for Pytorch Mobile to be able to deploy YOLO natively
