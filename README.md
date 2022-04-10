# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
# Step1:
Import cv2 and save and image as filename.jpg

# Step2:
Use imread(filename, flags) to read the file.

# Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

# Step4:
Split and merge the image using cv2.split and cv2.merge commands.

# Step5:
End the program and close the output image windows.

# PROGRAM:

Developed By: Lakshmi priya P
Register Number: 212221230053

# i) Convert BGR and RGB to HSV and GRAY:
```
import cv2
sun_color_image = cv2.imread('image.jpg')
cv2.imshow('Original image', sun_color_image)
hsv_image = cv2.cvtColor(sun_color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV' ,hsv_image )
gray_image1 = cv2.cvtColor (sun_color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()
```
# ii)Convert HSV to RGB and BGR
```
import cv2
sun_color_image = cv2.imread('image.jpg')
cv2.imshow('Original image', sun_color_image)
hsv_image = cv2.cvtColor(sun_color_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB' ,hsv_image )
gray_image1 = cv2.cvtColor (sun_color_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()
```
# iii)Convert RGB and BGR to YCrCb
```
import cv2
sun_color_image = cv2.imread('image.jpg')
cv2.imshow('Original image', sun_color_image)
gray_image1 = cv2.cvtColor (sun_color_image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb', gray_image1)
gray_image1 = cv2.cvtColor (sun_color_image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()
```
# iv)Split and Merge RGB Image
```
import cv2
image = cv2.imread('image.jpg')
blue=image[:,:,0]
green=image[:,:,1]
red=image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
Merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',Merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()
```
# v) Split and merge HSV Image
```
import cv2
image = cv2.imread('image.jpg')
hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue-Image',h)
cv2.imshow('Saturation-Image',s)
cv2.imshow('Gray-Image',v)
Merged_HSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()
```

## Output:
### i) BGR and RGB to HSV and GRAY
![output1](https://user-images.githubusercontent.com/93427923/162604461-7749be3f-6ee2-4e1f-9914-4f8c9e16254c.png)


### ii) HSV to RGB and BGR
![OUTPUT2](https://user-images.githubusercontent.com/93427923/162604471-14bb715e-7ca6-41e1-b1d6-ee72d8d105c4.png)


### iii) RGB and BGR to YCrCb
![OUTPUT3](https://user-images.githubusercontent.com/93427923/162604483-a58fb469-b9d0-4f3c-9c25-7bcf125ee962.png)


### iv) Split and merge RGB Image
![OUTPUT4 1](https://user-images.githubusercontent.com/93427923/162604487-5f10ec67-bcbe-4d0c-adac-e0c9bf0e75d7.png)
![OUTPUT4 2](https://user-images.githubusercontent.com/93427923/162604505-7250f6fb-5a6e-435e-b23d-fe859fd1dad4.png)

### v) Split and merge HSV Image
![OUTPUT5 1](https://user-images.githubusercontent.com/93427923/162604518-19898962-b03f-4771-bbd4-09dfb9ca5c33.png)
![OUTPUT5 2](https://user-images.githubusercontent.com/93427923/162604526-289a2e76-a180-4687-b0df-d10631090cf1.png)

## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
