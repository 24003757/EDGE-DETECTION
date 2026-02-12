# Experiment-6
# EDGE-DETECTION
### Developed by: VINOLIA ALAINA. R
### Register Number: 212224240184
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

### Developed by: VINOLIA ALAINA. R
### Register Number: 212224240184

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
<img width="635" height="441" alt="image" src="https://github.com/user-attachments/assets/b641bc81-6990-47d5-b88b-6fc5ce1c47fd" />
<img width="640" height="436" alt="image" src="https://github.com/user-attachments/assets/cf936df4-dbf2-40fa-808c-484fe9e444b7" />
<img width="645" height="445" alt="image" src="https://github.com/user-attachments/assets/773c4595-3df8-494f-a2da-e0c41c5b5a3f" />
<img width="658" height="443" alt="image" src="https://github.com/user-attachments/assets/ec2b98dc-e56f-483a-a060-3cd02f33a4f2" />



## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
