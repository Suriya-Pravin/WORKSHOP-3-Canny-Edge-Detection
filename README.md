# EDGE DETECTION USING PYTHON

## NAME: Suriya Pravin M  
## REGISTER NO: 212223230223

---

## AIM:
To perform various edge detection techniques on an input image using Python and OpenCV.

---

## PROCEDURE:
1. Import the required libraries such as OpenCV, NumPy, and Matplotlib.
2. Load the input image in grayscale mode.
3. Apply Sobel operator in both X and Y directions to detect edges.
4. Apply Laplacian operator to highlight image intensity variations.
5. Apply Canny edge detector with threshold values.
6. Display all detected edge results using Matplotlib.
7. Analyze and compare the results from different edge detection techniques.

## REQUIREMENTS:
- Python 3.x
- OpenCV
- Numpy
- Jupyter Notebook / Python Script

---

## PROGRAM:
```python
import cv2
import matplotlib.pyplot as plt

# Read Image
i = cv2.imread('boy.jpg', 0)

# Sobel Edge Detection
sobelx = cv2.Sobel(i, cv2.CV_64F, 1, 0, ksize=3)
sobely = cv2.Sobel(i, cv2.CV_64F, 0, 1, ksize=3)
sobel = sobelx + sobely

# Laplacian Edge Detection
laplacian = cv2.Laplacian(i, cv2.CV_64F)

# Canny Edge Detection
canny = cv2.Canny(i, 100, 200)

# Display Results
plt.figure(figsize=(10,10))
plt.subplot(2,2,1), plt.imshow(i, cmap='gray'), plt.title('Original Image')
plt.subplot(2,2,2), plt.imshow(sobel, cmap='gray'), plt.title('Sobel Edge')
plt.subplot(2,2,3), plt.imshow(laplacian, cmap='gray'), plt.title('Laplacian Edge')
plt.subplot(2,2,4), plt.imshow(canny, cmap='gray'), plt.title('Canny Edge')
plt.show()
```

---

## OUTPUT:

<img width="1906" height="738" alt="image" src="https://github.com/user-attachments/assets/a61c0d4c-5341-4ca7-8369-bd3e6433aecf" />

---

## RESULT:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
