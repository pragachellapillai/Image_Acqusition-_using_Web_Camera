# Image_Acqusition-_using_Web_Camera
## Aim
 
Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
<br>

### Step 2:
<br>

### Step 3:
<br>

### Step 4:
<br>

### Step 5:
<br>

## Program:
``` Python
### Developed By:N.C .PRAGAHARSHITHA
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

## ii) Display the video
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

## iii) Display the video by resizing the window
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

## iv) Rotate and display the video


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

![real image](https://github.com/pragachellapillai/Image_Acqusition-_using_Web_Camera/assets/148254952/76aa9891-db73-4097-9d0d-c9c84dd5ecda)


### ii) Display the video


![bfebe7](https://github.com/pragachellapillai/Image_Acqusition-_using_Web_Camera/assets/148254952/f10fd73c-7215-4729-af61-6eac75007eef)

### iii) Display the video by resizing the window


![WhatsApp Image 2024-03-07 at 08 40 05_66684ea7](https://github.com/pragachellapillai/Image_Acqusition-_using_Web_Camera/assets/148254952/6bd3685e-c045-4ccc-b7ab-2e60c98599f6)

### iv) Rotate and display the video


![1234](https://github.com/pragachellapillai/Image_Acqusition-_using_Web_Camera/assets/148254952/be1c67d5-2aeb-458c-9d1a-6bc5f9e88d76)




## Result:
Thus the image is accessed from webcamera and displayed using openCV.
