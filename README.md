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
Create the text image using cv2.putText.

### Step3:
Then create the structuring image for dilation/erosion.

### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate.

### Step5:
Plot the images using plt.imshow.
 
## Program:

``` Python
# Name: Ranjith D
# Reg no: 212221240044

# Import the necessary packages
import numpy as np
import cv2
# Create the Text using cv2.putText
img=np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
img1=cv2.putText(img,'Ranjith',(5,70),font,2,(255),5,cv2.LINE_AA)
cv2.imshow('original',img1)
cv2.waitKey(0)
cv2.destroyAllWindows()
# Create the structuring element
kernel = np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
# Erode the image
erode=cv2.erode(img1,kernel)
cv2.imshow('erode',erode)
cv2.waitKey(0)
cv2.destroyAllWindows()
# Dilate the image
dilate=cv2.dilate(img1,kernel1)
cv2.imshow('dilate',dilate)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:

### Display the input Image
![](https://github.com/RanjithD18/Implementation-of-Erosion-and-Dilation/blob/main/1.png)

### Display the Eroded Image
1[](https://github.com/RanjithD18/Implementation-of-Erosion-and-Dilation/blob/main/2.png)

### Display the Dilated Image
![](https://github.com/RanjithD18/Implementation-of-Erosion-and-Dilation/blob/main/3.png)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
