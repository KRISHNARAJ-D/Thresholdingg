# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image

## Program:
```
NAME: KRISHNARAJ D
REG NO: 212222230070
```
### Import the necessary packages
``` Python

import numpy as np
import cv2
import matplotlib.pyplot as plt
```

### Create the Text using cv2.putText
``` Python
img = np.zeros((100,400),dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,'KRISHNA',(40,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
### Create the structuring element
``` Python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
```
### Erode the image
``` Python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```
### Dilate the image
``` Python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:

### Display the input Image
![9 1](https://github.com/KRISHNARAJ-D/Thresholdingg/assets/119559695/c508596f-87e6-44a0-bf9e-46e231ffbefe)


### Display the Eroded Image

![9 2](https://github.com/KRISHNARAJ-D/Thresholdingg/assets/119559695/78bb1ab6-608d-4f0c-b0b1-4524395ff1af)

### Display the Dilated Image
![9 3](https://github.com/KRISHNARAJ-D/Thresholdingg/assets/119559695/1a6a4d37-93c1-40d9-8238-13582260a072)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
