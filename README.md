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
### Developed By   : Koti Sai Sankar
### Register Number: 212222240111
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("meme.jpg")
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


</br>

i) Using Averaging Filter

![image](https://github.com/KotiSaiSankar/Implementation-of-filter/assets/118344248/7f9cdbfa-8437-4bc1-a45b-4d7b06b34532)

</br>


ii) Using Weighted Averaging Filter
</br>

![image](https://github.com/KotiSaiSankar/Implementation-of-filter/assets/118344248/6c4baf12-7421-4466-adad-57e1947bc3ab)

iii) Using Gaussian Filter

![image](https://github.com/KotiSaiSankar/Implementation-of-filter/assets/118344248/9a9a4bd9-fb60-461d-887a-21cbde2558e2)

iv) Using Median Filter
</br>

![image](https://github.com/KotiSaiSankar/Implementation-of-filter/assets/118344248/706facd3-a6fc-4745-8370-1b3f3e116944)

</br>

### 2. Sharpening Filters

i) Using Laplacian Kernal
</br>
</br>
![image](https://github.com/KotiSaiSankar/Implementation-of-filter/assets/118344248/7bf3cabf-b6d0-451e-840b-f597fdbbf249)

</br>

ii) Using Laplacian Operator
</br>
![image](https://github.com/KotiSaiSankar/Implementation-of-filter/assets/118344248/f4b22a45-002a-4629-a10b-a04bafb82717)


</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
