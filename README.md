# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By: RAJA R
# Register Number: 212222100041

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("grays.jpg")
color_image = cv2.imread("Colour.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
Histogram of Grayscale Image
```
import numpy as np
import cv2
Gray_image = cv2.imread("grays.jpg")
Color_image = cv2.imread("colour.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
```
Histogram of Green channel of colour Image
```
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
Histogram Equalization of Grayscale Image
```

import cv2
gray_image = cv2.imread("colour.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### Input Grayscale Image and Color Image

![Screenshot 2024-03-19 111753](https://github.com/Raja8334/Histogram-of-an-images/assets/120719634/9eb0aff0-0cb5-4b27-adf7-1c6d2e765701)

![Screenshot 2024-03-19 111809](https://github.com/Raja8334/Histogram-of-an-images/assets/120719634/0b19d098-75d9-46a0-868c-eaf4704508f2)


### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2024-03-19 111924](https://github.com/Raja8334/Histogram-of-an-images/assets/120719634/abee02e8-c988-4790-8f28-8b7fff2aade8)

![Screenshot 2024-03-19 111938](https://github.com/Raja8334/Histogram-of-an-images/assets/120719634/c118274b-89bc-49c7-8f51-f11606de6905)

### Histogram of Green channel of Color Image
![Screenshot 2024-03-19 112019](https://github.com/Raja8334/Histogram-of-an-images/assets/120719634/fd1772f4-9b67-4d65-8976-5b71b255e18e)
![Screenshot 2024-03-19 112034](https://github.com/Raja8334/Histogram-of-an-images/assets/120719634/8a0badca-115f-4bf3-82ad-99aac58b545e)

### Histogram Equalization of Grayscale Image.

![Screenshot 2024-03-19 112134](https://github.com/Raja8334/Histogram-of-an-images/assets/120719634/dbcf276b-1680-4fee-b8f1-dd9539177c60)

![Screenshot 2024-03-19 112154](https://github.com/Raja8334/Histogram-of-an-images/assets/120719634/58f93dfc-e385-4653-955b-df342ca41e81)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
