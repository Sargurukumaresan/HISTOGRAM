# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.
### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.
### Step3:
Display the histograms with their respective images.
### Step4:
Equalize the grayscale image.
### Step5:
Display the grayscale image.
## Program:
```python
# Developed BySARGURU.K
# Register Number:212222230134
import cv2
import matplotlib.pyplot as plt
# Write your code to find the histogram of gray scale image and color image channels.
import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('is.jpeg')
plt.imshow(Gray_image)
plt.show()
color_image=cv2.imread('iss.jpeg')
plt.imshow(color_image)
plt.show()
# Display the histogram of gray scale image and any one channel histogram from color image
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("is.jpeg")
color_image = cv2.imread("iss.jpeg")
gray_hist = cv2.calcHist([gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()

plt.imshow(color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()

# Write the code to perform histogram equalization of the image. 
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread('is.jpeg',0)
equ=cv2.equalizeHist(gray_image)
cv2.imshow('Gray image',gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![ex43](https://github.com/BaskaranV15/HISTOGRAM/assets/118703522/9a88a65a-6351-4c6c-b26a-b02df25580d2)
![ex42](https://github.com/BaskaranV15/HISTOGRAM/assets/118703522/e39b88da-7bba-421f-adf7-fa09104c541b)
### Histogram of Grayscale Image and any channel of Color Image
![ex44](https://github.com/BaskaranV15/HISTOGRAM/assets/118703522/201bc531-ff9a-4003-9e44-9016d5a3b376)
![ex45](https://github.com/BaskaranV15/HISTOGRAM/assets/118703522/d69f98b5-d737-447f-8b27-40a132f2d9bc)
### Histogram Equalization of Grayscale Image
![ex4la](https://github.com/BaskaranV15/HISTOGRAM/assets/118703522/4914a216-e22f-4797-8513-2dd420854e6a)
## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
