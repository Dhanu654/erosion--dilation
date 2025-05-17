# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Create a blank image.


### Step2:
Create a structuring element (5x5 rectangular)
### Step3:
Erode the image.

### Step4:
Dilate the image.

### Step5:
End the program.

 
## Program:

~~~
# Developed By: DHANUSYA K
# Register No: 212223230043


import cv2
import numpy as np
from matplotlib import pyplot as plt
# Load the image
img1=np.zeros((100,700),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the text using cv2.putText
cv2.putText(img1,'DHANUSYA ' ,(5,70),font,4,(255),2,cv2.LINE_AA)


# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
img_erode=cv2.erode(img1,kernel1)

# Display the results
plt.figure(figsize=(12, 5))
plt.subplot(1,3,1)
plt.imshow(img1,cmap='gray')
plt.subplot(1,3,2)
plt.imshow(img_dilate,cmap='gray')
plt.subplot(1,3,3)
plt.imshow(img_erode,cmap='gray')
~~~




## Output:
### Display the input Image:
![Screenshot 2025-05-17 112629](https://github.com/user-attachments/assets/79adebf5-dc8c-4b00-a007-f369df69ada3)
### Display the Eroded Image
![Screenshot 2025-05-17 112635](https://github.com/user-attachments/assets/01001e3f-5c8d-47f3-8151-aa0c23fed0b8)
### Display the Dilated Image
![Screenshot 2025-05-17 112640](https://github.com/user-attachments/assets/fd22dfc4-e5e2-41ab-a1d2-841815bf1869)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
