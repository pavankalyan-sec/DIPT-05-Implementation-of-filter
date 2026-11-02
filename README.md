# DIPT-05-Implementation-of-filter
# Name: Pavan Kalyan P
# Reg No: 212225240104'


## Aim

To implement filters for smoothing and sharpening images in the spatial domain.

## Software Required

- Anaconda - Python 3.7
- OpenCV
- NumPy
- Matplotlib

## Algorithm

### Step 1
Import the required libraries.

### Step 2
Read the image and convert it from BGR to RGB.

### Step 3
Apply the required smoothing and sharpening filters to the image separately.

### Step 4
Plot and display the original and filtered images using `matplotlib.pyplot`.

### Step 5
End the program.

## Program

**Developed By:** Pavan Kalyan P

**Register Number:** 212225240104

## 1. Smoothing Filters

### i) Using Averaging Filter

```python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("myimage.jpeg")
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

### ii) Using Weighted Averaging Filter

```python
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
plt.show())
```

### iii) Using Gaussian Filter

```python
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

### iv) Using Median Filter

```python
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

## 2. Sharpening Filters

### i) Using Laplacian Linear Kernel

```python
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

### ii) Using Laplacian Operator

```python
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

## Output

### 1. Smoothing Filters

#### i) Using Averaging Filter
<img width="607" height="407" alt="image" src="https://github.com/user-attachments/assets/11f095a9-1d50-41a9-87ad-c608422428e2" />



#### ii) Using Weighted Averaging Filter

<img width="437" height="290" alt="image" src="https://github.com/user-attachments/assets/44612ad0-3bdf-4950-8a3e-8378995d443f" />



#### iii) Using Gaussian Filter

<img width="427" height="292" alt="image" src="https://github.com/user-attachments/assets/f5efcdcf-a681-4131-9030-c357670b3657" />



#### iv) Using Median Filter

<img width="591" height="387" alt="image" src="https://github.com/user-attachments/assets/eabf38bf-0466-4a5b-ab48-1c78b0f59cc2" />


### 2. Sharpening Filters

#### i) Using Laplacian Kernel

<img width="441" height="291" alt="image" src="https://github.com/user-attachments/assets/915460b2-d34c-480c-bab9-2253d6f51444" />



#### ii) Using Laplacian Operator

<img width="426" height="282" alt="image" src="https://github.com/user-attachments/assets/c24b44ee-9780-4f9f-a4e3-3127c9c08704" />



## Result

Thus, filters were implemented for smoothing and sharpening images in the spatial domain using OpenCV and Python.
