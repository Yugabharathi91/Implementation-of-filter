# Implementation-of-filter

### Developed By   :  YUGABHARATHI M
### Register Number: 212224230314

## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
</br>
Using Averaging Filter
</br> 

### Step2
</br>
Using Weighted Averaging Filter
</br> 

### Step3
</br>
Using Gaussian Filter
</br> 

### Step4
</br>
Using Median Filter
</br> 

### Step5
</br>
Using Laplacian Kernal
</br>

### Step6
</br>
Using Laplacian Operator
</br> 

## Program:

</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("rose.png")
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
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
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
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
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
iv)Using Median Filter
```
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
i) Using Laplacian Linear Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
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
```

laplacian=cv2.Laplacian(image2,cv2.CV_64F)
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
</br>

i) Using Averaging Filter
</br>
</br>
<img width="911" height="362" alt="image" src="https://github.com/user-attachments/assets/50f9b5e9-3d82-4252-be0a-d1fac7fbe9d1" />


</br>
</br>

ii)Using Weighted Averaging Filter
</br>
</br>
<img width="675" height="271" alt="image" src="https://github.com/user-attachments/assets/de9f9078-560c-436e-aee0-ac520015db56" />



</br>
</br>

iii)Using Gaussian Filter
</br>
</br>
<img width="704" height="290" alt="image" src="https://github.com/user-attachments/assets/e11059de-1d7e-48ce-ba34-dea5fb509069" />



</br>
</br>

iv) Using Median Filter
</br>
</br>
<img width="931" height="352" alt="image" src="https://github.com/user-attachments/assets/ee01aa6f-d9d5-4c85-9c78-31d8fd82498a" />


</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
</br>
<img width="649" height="266" alt="image" src="https://github.com/user-attachments/assets/2133016c-91e4-4dbe-b869-2c75d4d08f6b" />




</br>
</br>

ii) Using Laplacian Operator
</br>
</br>

<img width="670" height="268" alt="image" src="https://github.com/user-attachments/assets/52fa044a-fda6-423b-8b17-cf10720e3c04" />

</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
