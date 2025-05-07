
# EXP NO 8: THRESHOLDING

### Name: V Raksha dharanika
### Register No: 212223230167


## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Load the necessary packages.

### Step2:
Read the Image and convert to grayscale.

### Step3:
Use Global thresholding to segment the image.

### Step4:
Use Adaptive thresholding to segment the image.

### Step5:
Use Otsu's method to segment the image and display the results.

## Program

### Load the necessary packages
```py
import numpy as np
import matplotlib.pyplot as plt
import cv2
```
### Read the Image and convert to grayscale
```py
image = cv2.imread("leaves.jpg",1)
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
image_gray = cv2.imread("leaves.jpg",0)
```
### Use Global thresholding to segment the image
```py
ret,thresh_img1=cv2.threshold(image_gray,86,255,cv2.THRESH_BINARY)
ret,thresh_img2=cv2.threshold(image_gray,86,255,cv2.THRESH_BINARY_INV)
ret,thresh_img3=cv2.threshold(image_gray,86,255,cv2.THRESH_TOZERO)
ret,thresh_img4=cv2.threshold(image_gray,86,255,cv2.THRESH_TOZERO_INV)
ret,thresh_img5=cv2.threshold(image_gray,100,255,cv2.THRESH_TRUNC)
```
### Use Adaptive thresholding to segment the image
```py
thresh_img7=cv2.adaptiveThreshold(image_gray,255,cv2.ADAPTIVE_THRESH_MEAN_C,cv2.THRESH_BINARY,11,2)
thresh_img8=cv2.adaptiveThreshold(image_gray,255,cv2.ADAPTIVE_THRESH_GAUSSIAN_C,cv2.THRESH_BINARY,11,2)
```
### Use Otsu's method to segment the image 
```py
ret,thresh_img6=cv2.threshold(image_gray,0,255,cv2.THRESH_BINARY+cv2.THRESH_OTSU)
```
### Display the results
#### ORIGIONAL IMAGE
```py


plt.axis("off")
plt.title("Original Image")
plt.imshow(image)

```
![image](https://github.com/user-attachments/assets/538c9922-bbb9-4063-aa49-c06ea73b8dd9)

#### GREY IMAGE
```py


plt.axis("off")
plt.title("Gray Image")
plt.imshow(cv2.cvtColor(image_gray, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()
```
![image](https://github.com/user-attachments/assets/76ca044c-01cc-425e-90d3-d3c5319718cf)

#### Threshold Image (Binary)
```py


plt.axis("off")
plt.title("Threshold Image (Binary)")
plt.imshow(cv2.cvtColor(thresh_img1, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```
![image](https://github.com/user-attachments/assets/29497c0f-bd75-440f-a7f2-a61e4189efa9)



#### Threshold Image (Binary Inverse)
```py


plt.axis("off")
plt.title("Threshold Image (Binary Inverse)")
plt.imshow(cv2.cvtColor(thresh_img2, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```
![image](https://github.com/user-attachments/assets/444cebcb-f30a-481e-927b-b33d0f1b79eb)



#### Threshold Image (To Zero)
```py


plt.axis("off")
plt.title("Threshold Image (To Zero)")
plt.imshow(cv2.cvtColor(thresh_img3, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```
![image](https://github.com/user-attachments/assets/225a54be-bb25-4936-bc8f-37fdb048678b)


#### Threshold Image (To Zero-Inverse)
```py


plt.axis("off")
plt.title("Threshold Image (To Zero-Inverse)")
plt.imshow(cv2.cvtColor(thresh_img4, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```
![image](https://github.com/user-attachments/assets/8b1f5a91-2094-42e5-8060-2ad755f341f5)


#### Threshold Image (Truncate)
```py

plt.axis("off")
plt.title("Threshold Image (Truncate)")
plt.imshow(cv2.cvtColor(thresh_img5, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```
![image](https://github.com/user-attachments/assets/4b6a033e-8655-492d-a1ec-b4ff2ff82b00)


#### Otsu
```py
plt.axis("off")
plt.title("Otsu")
plt.imshow(cv2.cvtColor(thresh_img6, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```
![image](https://github.com/user-attachments/assets/ddb7fb66-e301-4276-9ba2-a733d381c14b)


#### Adaptive Threshold (Mean)
```py

plt.axis("off")
plt.title("Adaptive Threshold (Mean)")
plt.imshow(cv2.cvtColor(thresh_img7, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```
![image](https://github.com/user-attachments/assets/d6debc89-09c0-4e85-97a6-6f45cb54e347)


#### Adaptive Threshold (Gaussian)
```py
plt.axis("off")
plt.title("Adaptive Threshold (Gaussian)")
plt.imshow(cv2.cvtColor(thresh_img8, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```
![image](https://github.com/user-attachments/assets/e27447d2-81f9-4894-a773-eab6fa0d9c4b)


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
