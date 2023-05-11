# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
### Algorithm:
### Step 1:
Load the necessary packages requiured for the implemtation of erosion and dilation on an image.

### Step 2:
Create the text image for the implemtation of erosion and dilation using cv2.putText function.

### Step 3:
Create the structuring image for the implemtation of erosion and dilation on the text image.

### Step 4:
Apply the erosion and dilation to the text image using cv2.erode and cv2.dilate.

### Step 5:
Display the images of the erosion and dilation applied using the plt.imshow.

### Step 6:
End the program.
 
## Program:

``` 
Developed by : Sanjay S
Register Number: 212221230086
Program to implement Erosion and Dilation using Python and OpenCV.
```
```py
# Import the necessary packages:

import cv2
import numpy as np
import matplotlib.pyplot as plt

```
```py
# Create the Text using cv2.putText:

text_image = np.zeros((100,300),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SCRIPT_COMPLEX = 7
cv2.putText(text_image,"Richard",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Text Image")
plt.imshow(text_image,'magma')
plt.axis('off')

```

```py

# Create the structuring element:

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

```
```py

# Dilate the image:

image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Text Image")
plt.imshow(image_dilate,'magma')
plt.axis('off')

```

## Output:

### Display the input Image

![Screenshot 2023-05-11 112200](https://github.com/simbu07/Implementation-of-Erosion-and-Dilation/assets/94525786/191b7e73-0039-44d6-b82f-a7f82f1156b6)


### Display the Eroded Image

![Screenshot 2023-05-11 112212](https://github.com/simbu07/Implementation-of-Erosion-and-Dilation/assets/94525786/a36b7053-0696-434d-a8ef-1a1dafc91a9f)


### Display the Dilated Image
![Screenshot 2023-05-11 112227](https://github.com/simbu07/Implementation-of-Erosion-and-Dilation/assets/94525786/c2eed713-274d-414b-b3ef-ef6c1318e00e)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
