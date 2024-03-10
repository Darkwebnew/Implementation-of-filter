# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Install the open cv by using pip install opencv-python

### Step2
Import cv2 for reading and changing it smooth and sharpen image

### Step3
import numpy for give the width and size of a image

### Step4
import matplotlib.pyplot for display the image.

## Program:
### Developed By   : V.Sriram
### Register Number: 212222103002
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('test_image.jpeg')
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/121
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('ORIGINAL')
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('FILTERED')
plt.axis('off')
```
ii) Using Weighted Averaging Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('test_image.jpeg')
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/121
kernal2=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernal2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('ORIGINAL')
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('FILTERED')
plt.axis('off')
```
iii) Using Gaussian Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('test_image.jpeg')
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/121
image3=cv2.GaussianBlur(src=image2,ksize=(11,11),sigmaX=0,sigmaY=0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('ORIGINAL')
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title(' Gaussian Filter')
plt.axis('off')
```
iv) Using Median Filter
```

import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('test_image.jpeg')
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/121
image3=cv2.medianBlur(src=image2,ksize=11)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('ORIGINAL')
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Median Blur')
plt.axis('off')
```
### 2. Sharpening Filters
i) Using Laplacian Kernal
```

import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('test_image.jpeg')
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/121
kernal2=np.array([[0,1,0],[1,-4,1],[0,1,0]])
image3=cv2.filter2D(image2,-1,kernal2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('ORIGINAL')
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Sharpening Filters')
plt.axis('off')
```
ii) Using Laplacian Operator
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('test_image.jpeg')
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/121
image3=cv2.Laplacian(image2,cv2.CV_64F)
laplacian_image = np.uint8(np.absolute(image3))
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('ORIGINAL')
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(laplacian_image)
plt.title('Sharpening Filters')
plt.axis('off')
```
## OUTPUT:
### 1. Smoothing Filters

i) Using Averaging Filter

![image](https://github.com/Darkwebnew/Implementation-of-filter/assets/143114486/14c38079-b9f6-4961-b5aa-a79f856b31ef)

ii) Using Weighted Averaging Filter

![image](https://github.com/Darkwebnew/Implementation-of-filter/assets/143114486/e26db09b-dcf9-47e0-bc0e-b38660e5003a)

iii) Using Gaussian Filter

![image](https://github.com/Darkwebnew/Implementation-of-filter/assets/143114486/81b80e6f-87e7-4968-bb19-ad47564ac032)

iv) Using Median Filter

![image](https://github.com/Darkwebnew/Implementation-of-filter/assets/143114486/a7de7a0d-9d9d-4057-843b-97a8f1ced3fc)

### 2. Sharpening Filters

i) Using Laplacian Kernal

![image](https://github.com/Darkwebnew/Implementation-of-filter/assets/143114486/7f2bb5a0-ee9a-4c25-a9de-aeadeaf9d1fe)

ii) Using Laplacian Operator

![image](https://github.com/Darkwebnew/Implementation-of-filter/assets/143114486/a86dd236-f057-4a6c-b56e-0650596330e9)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
