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
```py
Developed By   : Jerowin Geo J A
Register Number: 212223100016
```
### 1. Smoothing Filters

i) Using Averaging Filter
```Python

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("rome.jpg")
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

## i) Using Averaging Filter


![image](https://github.com/user-attachments/assets/61c2f1e6-0f7a-406b-ac05-7867df203215)



## ii) Using Weighted Averaging Filter

![image](https://github.com/user-attachments/assets/b0d19fe3-fbd8-4517-b4cc-349f6ce8637b)




## iii) Using Gaussian Filter

![image](https://github.com/user-attachments/assets/e0a24262-36f2-475e-886b-2fd480353711)




## iv) Using Median Filter

![image](https://github.com/user-attachments/assets/5076dc66-61ca-4714-8cef-2f9b1d4041a2)




### 2. Sharpening Filters

## i) Using Laplacian Kernal

![image](https://github.com/user-attachments/assets/89d30b17-bcde-43d0-818d-a3952e2a9b30)



## ii) Using Laplacian Operator

![image](https://github.com/user-attachments/assets/9ceca164-6088-4c74-a9cd-c9e0f19e7846)




## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.


