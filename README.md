# Driver-drowsiness-detection
A computer vis system made with the help of opencv that can automatically detect driver drowsiness in a real-time video stream and then play an alarm if the driver appears to be drowsyion
## Applications
### This can be used by riders who tends to drive the vehicle for a longer period of time that may lead to accidents
## Code Requirements
### The example code is in Python
## Dependencies
```
 1)import cv2
 2)import immutils
 3)import dlib
 4)import scipy
 5)import playsound
 6)import queue
 7)import time
 8)import sys
 ```
## Description
###  A computer vision system made with the help of opencv that can automatically detect driver drowsiness in a real-time video stream and then play an alarm if the driver appears to be drowsy.
## Algorithm
● We utilised a pre trained frontal face detector from Dlib’s library which is based on  a modification to the Histogram of Oriented Gradients in combination with Linear  SVM for classification.  

● The pre-trained facial landmark detector inside the dlib library is used to estimate  the location of 68 (x, y)-coordinates that map to facial structures on the face. The 68  landmark output is shown in the figure below. However, we utilised the 70 landmark  model.

<img src="https://github.com/shubham769/Driver-drowsiness-detection/blob/master/Images/face.PNG">

● We then calculate the aspect ratio to check whether eyes are opened or closed.

● The eye is open if Eye Aspect ratio is greater than threshold. (Around 0.3)

<img src="https://github.com/shubham769/Driver-drowsiness-detection/blob/master/Images/eye.PNG">

● A blink is supposed to last 200-300 milliseconds.

● A drowsy blink would last for  800-900  ms. 

<img src="https://github.com/shubham769/Driver-drowsiness-detection/blob/master/Images/eye_aspect_ratio.PNG">

## Execution
To run the code, run 
```
python blinkDetect.py
```
<video src="https://github.com/shubham769/Driver-drowsiness-detection/blob/master/Drowniness.mp4">
