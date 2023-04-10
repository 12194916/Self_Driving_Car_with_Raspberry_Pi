# Self_Driving_Car_with_Raspberry_Pi
We will train AI model for self-driving car that will work raspberry pi.

1.Collect and label traffic data: We used roborflow web site. 
![image](https://user-images.githubusercontent.com/90163078/230847600-e3ebdcc2-ae7f-4d95-8f9b-99de40753870.png)

2.Train
YOLO model: Next, the YOLO model is trained using the  data. The model
is trained to detect and classify different types of traffic signs. we used
YOLOv8.

![Traffic_sign_detection.GIF](Detection_with_YOLOv8/Road_signs_Detection.gif)

3.Convert
YOLO model to TensorFlow: After the YOLO model is trained, it needs to be
converted to TensorFlow format. This can be done using the
"convert.py" script from the repository of YOLO

4.Optimize
TensorFlow model for TensorFlow Lite: TensorFlow Lite is a lightweight version
of TensorFlow designed for mobile and embedded devices. To use the YOLO model
in ROS, it needs to be optimized for TensorFlow Lite.

5.Convert TensorFlow model to TensorFlow Lite: Once the TensorFlow model is optimized,
it can be converted to TensorFlow Lite format using the "tflite_convert"command provided 
by TensorFlow.

6.We measure the distance by the
size of the bounding boxes. We equal its shape to certain variable, so
according to its change the car will act. As you know, as it comes near,
bounding box will be bigger, so in some threshold, it will send a request to
the car system.
