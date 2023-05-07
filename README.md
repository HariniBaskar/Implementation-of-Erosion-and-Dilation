# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1:
Import the necessary packages.

### Step 2:
Create the text image using cv2.putText.

### Step 3:
Then create the structuring image for dilation/erosion.

### Step 4:
Apply erosion and dilation using cv2.erode and cv2.dilate.

### Step 5:
Plot the images using plt.imshow.
 
## Program:

```
Developed by : Harini.B
Register Number : 212221230035
```

```
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
text_image = np.zeros((100,440),dtype = 'uint8')
img=cv2.cvtColor(text_image,cv2.COLOR_BGR2RGB)
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(img,"Harini.B",(5,70),font,2,(0,0,255),5,cv2.LINE_AA)
cv2.imshow("Original Image",img)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
image_erode = cv2.erode(img,kernel)
cv2.imshow("Eroded Image",image_erode)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Dilate the image
image_dilate = cv2.dilate(img,kernel)
cv2.imshow("Dilated Image",image_dilate)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:

### Display the input Image
![out1](https://user-images.githubusercontent.com/93427253/236669347-336fee39-7620-4ade-9cff-d11453edfeae.png)

### Display the Eroded Image
![out2](https://user-images.githubusercontent.com/93427253/236669366-0148af89-e225-48b8-b2f3-991f4002c2f8.png)

### Display the Dilated Image
![out3](https://user-images.githubusercontent.com/93427253/236669426-9e98126a-5b8d-4ff4-a001-35972ed1adb9.png)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
