# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.


### Step2
Convert the image from BGR to RGB.


### Step3
Apply the required filters for the image separately.


### Step4
Plot the original and filtered image by using matplotlib.pyplot.


### Step5
End the program.


## Program:
### Developed By   : Abishek Xavier A
### Register Number: 212222230004
### 1. Smoothing Filters

i) Using Averaging Filter
```Python

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("nebula.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()

```
ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()




```
iii) Using Gaussian Filter
```Python

gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()



```

iv) Using Median Filter
```Python

median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()



```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python

kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()



```
ii) Using Laplacian Operator
```Python


laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()


```

## OUTPUT:
### 1. Smoothing Filters
i) Using Averaging Filter

![Screenshot 2024-03-19 144107](https://github.com/AbishekAnand15/Implementation-of-filter/assets/118706942/071a94f7-1c98-4cc5-aa51-da1084d64274)

ii) Using Weighted Averaging Filter

![Screenshot 2024-03-19 144112](https://github.com/AbishekAnand15/Implementation-of-filter/assets/118706942/4ebdd6e6-e027-41da-a476-6ddf2cf3d51f)

iii) Using Gaussian Filter

![Screenshot 2024-03-19 144136](https://github.com/AbishekAnand15/Implementation-of-filter/assets/118706942/59b7b210-b6d9-4631-9991-94c2c99e090b)

iv) Using Median Filter

![Screenshot 2024-03-19 144145](https://github.com/AbishekAnand15/Implementation-of-filter/assets/118706942/96f13828-7803-4313-ba03-a813f355ef9a)


### 2. Sharpening Filters

i) Using Laplacian Kernal

![Screenshot 2024-03-19 144150](https://github.com/AbishekAnand15/Implementation-of-filter/assets/118706942/a148ef5c-5076-4c92-bf00-33f3dbece1d0)

ii) Using Laplacian Operator


![Uploading Screenshot 2024-03-19 144156.png…]()

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
