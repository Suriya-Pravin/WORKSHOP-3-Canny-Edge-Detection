# CANNY EDGE DETECTION USING PYTHON

## NAME: Suriya Pravin M  
## REGISTER NO: 212223230223


## AIM:
To perform various edge detection techniques on an input image using Python and OpenCV.


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


## PROGRAM:
```python
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('boy.jpg',cv2.IMREAD_GRAYSCALE)
blurred =cv2.GaussianBlur(img, (5,5),0)
edges = cv2.Canny(blurred, 50, 150)
plt.figure(figsize=(10,5))
plt.subplot(121),plt.imshow(img, cmap='gray')
plt.title('Original Image'), plt.axis('off')
plt.subplot(122),plt.imshow(edges, cmap='gray')
plt.title('Detected Edges'), plt.axis('off')
plt.show()
```



## OUTPUT:

<img width="1906" height="738" alt="image" src="https://github.com/user-attachments/assets/a61c0d4c-5341-4ca7-8369-bd3e6433aecf" />


## RESULT:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
