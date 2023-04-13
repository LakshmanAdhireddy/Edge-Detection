# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
Step 1:
Import the necessary modules.

Step 2:
For performing edge detection on a image.

Sobel
sobelx=cv2.Sobel(gray,cv2.CV_64F,1,0,5)
sobely=cv2.Sobel(gray,cv2.CV_64F,0,1,5)
sobelxy=cv2.Sobel(gray,cv2.CV_64F,1,1,5)

Laplacian

lap=cv2.Laplacian(gray,cv2.CV_64F)

Canny

canny=cv2.Canny(gray,120,150)

Step 3:
Display all the images with their respective edge detected images.
 
## Program:

``` Python
### Developed by :Lakshman
### register nuber :212222240001

# Import the packages
import cv2
import matplotlib.pyplot as plt


# Load the image, Convert to grayscale and remove noise

img=cv2.imread("pk.jpeg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)

# SOBEL EDGE DETECTOR

sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()

sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()

sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()

# LAPLACIAN EDGE DETECTOR

lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()

# CANNY EDGE DETECTOR
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()

```
## Output:
### SOBEL EDGE DETECTOR
![OUTPUT](/1.png)

### LAPLACIAN EDGE DETECTOR
![OUTPUT](/2.png)


### CANNY EDGE DETECTOR
![OUTPUT](/3.png)
## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
