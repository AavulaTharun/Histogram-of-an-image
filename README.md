# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image

Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.

Step3:
Display the histograms with their respective images.

Step4:
Equalize the grayscale image.

Step5:
Display the grayscale image.

## Program:
```python
# Developed By:Aavula Tharun
# Register Number:212221240003
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.

gray_image = cv2.imread("butterfly.jpg")
plt.imshow(gray_image)
plt.show()
hist=cv2.calcHist([gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('Grayscale value')
plt.ylabel('Pixel Count')
plt.stem(hist)
plt.show()



# Display the histogram of gray scale image and any one channel histogram from color image

color_image=cv2.imread("venice.jpg")
plt.imshow(color_image)
plt.show()
hist1=cv2.calcHist([color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(hist1)
plt.show()



# Write the code to perform histogram equalization of the image. 


gray_image = cv2.imread('butterfly.jpg',0)
equ=cv2.equalizeHist(gray_image)
cv2.imshow('Gray image',gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()




```
## Output:
### Input Grayscale Image and Color Image

![!](https://user-images.githubusercontent.com/93427201/164982144-33b878ae-4508-43ee-b06f-1b410d9ecac5.png)

### Histogram of Grayscale Image and any channel of Color Image

![!!](https://user-images.githubusercontent.com/93427201/164982167-03b58bca-872b-4a40-ae10-92c6a37be4da.png)

### Histogram Equalization of Grayscale Image

![!!!](https://user-images.githubusercontent.com/93427201/164982184-a365ad4a-1c5f-4529-a41c-506bc9abcbfb.png)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
