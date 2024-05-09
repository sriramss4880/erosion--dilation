# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the Image

### Step5:
Dilate the Image

 
## Program:
```
Name: SRIRAM S S
Reg No: 212222230150

# Import the necessary packages
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```


# Create the Text using cv2.putText
```python
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'Good',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```


# Create the structuring element
```python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```


# Erode the image
```python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```



# Dilate the image
```python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:

### Display the input Image
![image](https://github.com/Gokul0117/erosion--dilation/assets/121165938/fd742812-32bd-4590-808e-ba0ce7b21c42)


### Display the Eroded Image
![image](https://github.com/Gokul0117/erosion--dilation/assets/121165938/85f9d0af-fc2a-4eb4-a183-d31e715cec16)


### Display the Dilated Image
![image](https://github.com/Gokul0117/erosion--dilation/assets/121165938/e669b7dd-b458-4024-87b2-71e880e4895a)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
