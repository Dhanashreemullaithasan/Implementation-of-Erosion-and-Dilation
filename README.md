# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:

Import the necessary packages.

### Step2:

Create the Text using cv2.putText.

### Step3:

Create the structuring element.

### Step4:

Erode the image using cv2.erode().

### Step5:

Dilate the image using cv2.dilate().

 
## Program:

``` Python
# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText

img1=np.zeros((90,250),dtype='uint8')
img2=cv2.cvtColor(img1,cv2.COLOR_BGR2RGB)
font=cv2.FONT_HERSHEY_DUPLEX
cv2.putText(img2,'JANANI',(5,70),font,2,(218, 112, 214),3,cv2.LINE_8)
plt.imshow(img2)


# Create the structuring element

kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image

image_erode1=cv2.erode(img2,kernel1)
plt.imshow(image_erode1)

# Dilate the image

image_dilate=cv2.dilate(img2,kernel1)
plt.imshow(image_dilate)


```
## Output:

### Display the input Image
![dipimm1](https://github.com/Dhanashreemullaithasan/Implementation-of-Erosion-and-Dilation/assets/94165415/ad8f2f70-7efa-41ce-96a0-fac53368b710)


### Display the Eroded Image
![dipim2](https://github.com/Dhanashreemullaithasan/Implementation-of-Erosion-and-Dilation/assets/94165415/c074e6ad-cedb-439a-a49f-cec6fe43170f)


### Display the Dilated Image
![dipim3](https://github.com/Dhanashreemullaithasan/Implementation-of-Erosion-and-Dilation/assets/94165415/128b6657-231a-4325-b696-a05d7c276b9b)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
