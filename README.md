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

![Screenshot 2024-03-19 143808](https://github.com/AbishekAnand15/Implementation-of-filter/assets/118706942/dfc719dc-f6e4-468b-8241-8c7a52f6ba2a)

ii) Using Weighted Averaging Filter

![Screenshot 2024-03-19 143813](https://github.com/AbishekAnand15/Implementation-of-filter/assets/118706942/e45ed662-9fcf-46e3-b1a6-a457fa7081ff)

iii) Using Gaussian Filter

![Screenshot 2024-03-19 143819](https://github.com/AbishekAnand15/Implementation-of-filter/assets/118706942/3d5a3140-195d-4e36-a545-468d395dd817)

iv) Using Median Filter

![Screenshot 2024-03-19 143826](https://github.com/AbishekAnand15/Implementation-of-filter/assets/118706942/5c26fb2b-b070-48bc-ada9-4493cb1b85d5)


### 2. Sharpening Filters

i) Using Laplacian Kernal

![Screenshot 2024-03-08 155955](https://github.com/vinodkumar-s/Implementation-of-filter/assets/113497226/70e772fa-a2c5-46e7-b87f-2c3f56becb55)

ii) Using Laplacian Operator

![Screenshot 2024-03-08 160015](https://github.com/vinodkumar-s/Implementation-of-filter/assets/113497226/dcbc8a0c-ef89-44d2-837a-158b0e5ad966)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
