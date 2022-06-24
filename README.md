### EX NO : 10
### DATE  : 28.05.2022
# <p align="center">Implementation-of-Erosion-and-Dilation</p>

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
Erode and Dilate the image.
### Step5:
End Program.

<br>
<br>
<br>
<br>
<br>
<br>

## Program:
``` Python
# Developed By:J Vincent isaac jeyaraj
# Register Number: 212220230060

# Import the necessary packages
import cv2
import matplotlib.pyplot as plt
import numpy as np

# Create the Text using cv2.putText
img1=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX
cv2.putText(img1,'Vincent',(5,70),font,2,(255),5,cv2.LINE_AA)

# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
image_erode=cv2.erode(img1,kernel)
plt.imshow(image_erode)
plt.axis('off')
plt.title('Erosion')

# Dilate the image
image_dilate=cv2.dilate(img1,kernel)
plt.imshow(image_dilate)
plt.axis('off')
plt.title('Dilation')
```
## Output:

### Display the input Image
![Capture19](https://user-images.githubusercontent.com/75234588/169644184-875b90e8-23fa-4344-90a9-161a046e5853.PNG)

<br>
<br>
<br>
<br>
<br>

### Display the Eroded Image
![Capture20](https://user-images.githubusercontent.com/75234588/169644189-46e36b59-3a01-48b4-92fe-18eb4a01fc31.PNG)

### Display the Dilated Image
![Capture19](https://user-images.githubusercontent.com/75234588/169644190-29fdd912-f1b2-406d-9243-219de48932ff.PNG)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
