# EXP-6 EDGE DETECTION
## Name : P PARTHIBAN
### Register No : 212223230145
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:
Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.


## Program :

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('image.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

<img width="389" height="409" alt="download" src="https://github.com/user-attachments/assets/13a2b5d7-8893-4cf2-be3b-e63b873a26e8" />


### SOBEL EDGE DETECTOR

```python
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
<img width="389" height="409" alt="download" src="https://github.com/user-attachments/assets/3d0422d0-a9dd-4de1-b645-83701a8308c1" />



### LAPLACIAN EDGE DETECTOR

```python
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
<img width="389" height="409" alt="download" src="https://github.com/user-attachments/assets/9d37a723-7995-4ebf-b6d5-a190f0604853" />



### CANNY EDGE DETECTOR

```python
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
<img width="389" height="409" alt="download" src="https://github.com/user-attachments/assets/65ae8938-f260-4e6e-a590-cfd0700cbf0f" />



## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
