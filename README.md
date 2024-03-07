# Image_Acqusition-_using_Web_Camera
### Aim
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations. i) Write the frame as JPG ii) Display the video iii) Display the video by resizing the window iv) Rotate and display the video

### Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Use cv2.VideoCapture(0) to access web camera
### Step 2:
Use cv2.imread to read the video or image
### Step 3:
Use cv2.imwrite to save the image
### Step 4:
Use cv2.imshow to show the video
### Step 5:
End the program and close the output video window by pressing 'q'

## Program:
### Developed By:N C .PRAGAHARSHITHA
### Register No:212222110033
## i) Write the frame as JPG file
```
import cv2
viedoCaptureObject=cv2.VideoCapture(0)
while(True):
    ret,frame=viedoCaptureObject.read()
    cv2.imwrite("anbu.jpg",frame)
    result=False
viedoCaptureObject.release()
cv2.destroyAllWindows()
```
### ii) Display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('lion',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
### iii) Display the video by resizing the window
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222240009_anbu',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
### iv) Rotate and display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222240009_anbu',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## Output
### i) Write the frame as JPG image
![real image](https://github.com/pragachellapillai/Image_Acqusition-_using_Web_Camera/assets/148254952/09e53093-1c87-4292-92e2-32ee58163034)
### ii) Display the video
![bfebe7](https://github.com/pragachellapillai/Image_Acqusition-_using_Web_Camera/assets/148254952/96e7290d-fa9d-403c-950d-f978f51bd549)
### iii) Display the video by resizing the window
![WhatsApp Image 2024-03-07 at 08 40 05_66684ea7](https://github.com/pragachellapillai/Image_Acqusition-_using_Web_Camera/assets/148254952/7cdcd313-f350-4223-86ef-7dfd2da9507e)
### iv) Rotate and display the video
![1234](https://github.com/pragachellapillai/Image_Acqusition-_using_Web_Camera/assets/148254952/a93c70f6-7e9b-464c-a0b9-a86216c321f5)
## Result:
Thus the image is accessed from webcamera and displayed using openCV.
