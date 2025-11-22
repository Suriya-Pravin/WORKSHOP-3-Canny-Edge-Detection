# CANNY EDGE DETECTION USING PYTHON

## NAME: Suriya Pravin M  
## REGISTER NO: 212223230223


## AIM:
To detect edges in an image using Canny edge detection.


## PROCEDURE:

1. Import required libraries: OpenCV and Matplotlib.
2. Load the input image in grayscale format.
3. Apply Gaussian Blur to reduce image noise.
4. Perform Canny Edge Detection with appropriate threshold values.
5. Display both the original and edge-detected images.
6. Analyze the detected edges.


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
Thus, edges of the input image were successfully detected using Canny edge detection techniques.
