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
# Developed By: KRITHIGA U
# Register Number: 212223240076
```
# Grayscale image and Color image
```
#Grayscale image and Color image
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("MODEL.png")
color_image = cv2.imread("MODEL_2.png",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# Histogram of Grayscale image and color image
```
#Histogram of Grayscale image and color image
import numpy as np
Gray_image = cv2.imread("MODEL.png")
Color_image = cv2.imread("MODEL_2.jpg")
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
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
# Histogram equalization of Grayscale image
```
#Histogram equalization of Grayscale image

gray_image = cv2.imread("smillepathi.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image

![Screenshot 2025-04-09 112254](https://github.com/user-attachments/assets/85a30373-07b8-488f-b9b9-eada01ab5fdc)

![Screenshot 2025-04-09 135541](https://github.com/user-attachments/assets/19a9401e-47a5-4363-81fc-a6520c69e01e)

### Histogram of Grayscale Image and any channel of Color Image

![Screenshot 2025-04-09 135904](https://github.com/user-attachments/assets/97741be4-171b-4748-bde4-d82b80540f29)

![Screenshot 2025-04-09 135914](https://github.com/user-attachments/assets/6f882b64-487c-4d50-92f2-887af79eb8fe)


### Histogram Equalization of Grayscale Image.

![Screenshot 2025-04-09 135618](https://github.com/user-attachments/assets/c2dde53d-7475-441a-bc10-48bf3dbc4a9b)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
