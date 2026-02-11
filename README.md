# Exp-6
# EDGE-DETECTION
### Developed by: ABISHEIK RAJ J 
### Register Number: 212224230006
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

## Program:

### Developed by: HASNA MUBARAK AZEEM
### Register Number: 2122223240052

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('hasna.jpeg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```

## Output:
<img width="357" height="460" alt="image" src="https://github.com/user-attachments/assets/a6537f4e-2534-481e-8e3c-b355c630c15e" />

<img width="363" height="464" alt="image" src="https://github.com/user-attachments/assets/289979d6-5486-4f4f-ba51-dc7f9f2810d1" />

<img width="355" height="458" alt="image" src="https://github.com/user-attachments/assets/c27010a8-fbb3-49a0-83d2-db01dd8a412d" />

<img width="360" height="464" alt="image" src="https://github.com/user-attachments/assets/cc106e1f-23e9-4efa-a92f-033722fa2642" />





## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
