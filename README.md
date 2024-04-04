# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Install the open cv by using pip install opencv-python

### Step2:
Import cv2 for reading and changing it smooth and sharpen image

### Step3:
Import numpy for give the width and size of a image

### Step4:
import matplotlib.pyplot for display the image.


## Program:
### Developed By   : SASIRAJKUMAR T J
### Register Number:212222230137
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("animal.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernal = np.ones((11,11),np.float32)/121
img2 = cv2.filter2D(img1,-1,kernal)

plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(img2)
plt.title('Filtered')
plt.axis('off')




```
ii) Using Weighted Averaging Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("animal.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernal2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
img2 = cv2.filter2D(img1,-1,kernal2)

plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(img2)
plt.title('Filtered')
plt.axis('off')




```
iii) Using Gaussian Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("animal.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
gaussian_blur =  cv2.GaussianBlur(src=img1,ksize=(11,11),sigmaX=0,sigmaY=0)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title('Filtered')
plt.axis('off')




```

iv) Using Median Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("animal.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
median = cv2.medianBlur(src=img1,ksize=11)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(median)
plt.title('Filtered')
plt.axis('off')




```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("animal.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernal3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
img3 = cv2.filter2D(img1,-1,kernal3)

plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(img3)
plt.title('Filtered')
plt.axis('off')





```
ii) Using Laplacian Operator
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("animal.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernal3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
img3 = cv2.filter2D(img1,-1,kernal3)
new_img = cv2.Laplacian(img1,cv2.CV_64F)

plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(new_img)
plt.title('Filtered')
plt.axis('off')




```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
![Screenshot 2024-04-04 085211](https://github.com/SASIRAJ27/Implementation-of-filter/assets/113497176/5b4c4b9d-3fa7-4a4d-b9af-100d43b410e0)


ii) Using Weighted Averaging Filter

![Screenshot 2024-04-04 085228](https://github.com/SASIRAJ27/Implementation-of-filter/assets/113497176/a77e9b67-d4b9-4ed5-b226-2c6318f604e8)


iii) Using Gaussian Filter
![Screenshot 2024-04-04 085234](https://github.com/SASIRAJ27/Implementation-of-filter/assets/113497176/fe81d5a2-8a8c-4289-af40-9b66a9269753)


iv) Using Median Filter
![Screenshot 2024-04-04 085239](https://github.com/SASIRAJ27/Implementation-of-filter/assets/113497176/1df71497-586f-4e0c-8d3e-554d3158e53f)


### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
![Screenshot 2024-04-04 085244](https://github.com/SASIRAJ27/Implementation-of-filter/assets/113497176/a9a4217e-610b-440f-9988-9503fb29138d)



ii) Using Laplacian Operator
![Screenshot 2024-04-04 085250](https://github.com/SASIRAJ27/Implementation-of-filter/assets/113497176/085a0cbc-38d0-4f57-88cf-5ceec0732eae)




## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
