# Edge-Detection
## AIM:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## SOFTWARE REQUIRED:
Anaconda - Python 3.7

## ALGORITHM:
### Step 1:
Import the necessary modules.

### Step 2:
For performing edge detection on a image. 
- Sobel 
```python
sobelx=cv2.Sobel(gray,cv2.CV_64F,1,0,5)
sobely=cv2.Sobel(gray,cv2.CV_64F,0,1,5)
sobelxy=cv2.Sobel(gray,cv2.CV_64F,1,1,5)
```
- Laplacian
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
```
- Canny
```python
canny=cv2.Canny(gray,120,150)
```

### Step 3:
Display all the images with their respective edge detected images.

## PROGRAM:
```
/*
Developed by: B.Kavya
Registration Number : 212220230007
*/
```

``` Python
# Import the packages
import cv2
import matplotlib.pyplot as plt

# Load the image, Convert to grayscale and remove noise
img=cv2.imread("img.jpg",0)
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
## OUTPUT:
### SOBEL EDGE DETECTOR
![image](https://user-images.githubusercontent.com/75235813/168632082-49e2af4d-1366-4f74-b04a-b2995a5b7daf.png)

![image](https://user-images.githubusercontent.com/75235813/168632144-d6216e1f-d39a-4927-9adc-a7bbba054762.png)

![image](https://user-images.githubusercontent.com/75235813/168632190-f58f2345-1993-4734-a4b3-4f9444a0c1bf.png)


### LAPLACIAN EDGE DETECTOR

![image](https://user-images.githubusercontent.com/75235813/168632265-b39da731-c921-48e2-bda4-182f20df3a38.png)


### CANNY EDGE DETECTOR

![image](https://user-images.githubusercontent.com/75235813/168632357-45f498f0-5474-411b-951a-cdd63e1e6f0f.png)


## RESULT:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
