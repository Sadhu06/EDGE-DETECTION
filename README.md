## EDGE-DETECTION

## NAME : SADHANA S
## REGISTER NUMBER : 212224230234

## Aim

To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required

- Anaconda - Python 3.7
- OpenCV
- NumPy
- Matplotlib

## Algorithm

### Step 1
Import all the necessary modules for the program.

### Step 2
Load an image using the `cv2.imread()` function.

### Step 3
Convert the image into grayscale using `cv2.cvtColor()`.

### Step 4
Use the Sobel operator from OpenCV to detect the edges of the image in the horizontal and vertical directions.

### Step 5
Use the Laplacian operator to detect edges based on second-order derivatives.

### Step 6
Use the Canny operator to detect edges in the image.

### Step 7
Display the edge-detected images using Matplotlib.

## Program

**Developed By:** SADHANA S

**Register Number:** 212224230234

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread(r'C:\Users\admin\Downloads\mypic.jpeg')

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Original Image
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')

# Sobel Edge Detection
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)
sobel_combined = cv2.magnitude(sobel_x, sobel_y)

plt.subplot(2, 2, 2)
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')

# Laplacian Edge Detection
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)

plt.subplot(2, 2, 3)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')

# Canny Edge Detection
canny_edges = cv2.Canny(gray_image, 50, 150)

plt.subplot(2, 2, 4)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')

plt.tight_layout()
plt.show()

```

## Output

### Input Image 

<img width="299" height="299" alt="image" src="https://github.com/user-attachments/assets/0824fcdd-3487-4898-910f-4bc0d043f4e9" />



### 1. Sobel Edge Detector


<img width="272" height="299" alt="image" src="https://github.com/user-attachments/assets/cf7ef45c-a6a4-4869-8095-ac213b911101" />



### 2. Laplacian Edge Detector


<img width="342" height="317" alt="image" src="https://github.com/user-attachments/assets/84f2d515-cfb5-452e-9f12-b8f39ed174b3" />



### 3. Canny Edge Detector


<img width="307" height="308" alt="image" src="https://github.com/user-attachments/assets/1c1ee9d2-debf-4f28-a61f-052dfd68c5f3" />



## Result

Thus, the edges of the image were detected successfully using Sobel, Laplacian, and Canny edge detectors with OpenCV and Python.
