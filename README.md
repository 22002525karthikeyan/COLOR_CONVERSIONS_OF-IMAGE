# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
o	Draw a line from the top-left to the bottom-right of the image.
o	Draw a circle at the center of the image.
o	Draw a rectangle around a specific region of interest in the image.
o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
o	Convert the image from RGB to HSV and display it.
o	Convert the image from RGB to GRAY and display it.
o	Convert the image from RGB to YCrCb and display it.
o	Convert the HSV image back to RGB and display it.

### Step4:
o	Access and print the value of the pixel at coordinates (100, 100).
o	Modify the color of the pixel at (200, 200) to white.

### Step5:
o	Resize the original image to half its size and display it.
### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
o	Flip the original image horizontally and display it.
o	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.


##### Program:
### Developed By:
### Register Number: 


## Output:

### i)Read and Display an Image
```
import cv2 
image=cv2.imread('iron.jpg',1)
image =cv2.resize(image, (400, 300))
cv2.imshow('WINDOW',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/0534ac98-7bd7-4ec6-8296-9ea2d5a9b9be)

### ii)Draw Shapes and Add Text
#### Draw a line from the top-left to the bottom-right of the image.
```
import cv2
image = cv2.imread("iron.jpg")
image = cv2.resize(image, (400, 300))
res = cv2.line(image, (0, 0), (image.shape[1], image.shape[0]), (255,0,0), 10)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/7ac4d605-24a4-49b8-9d03-9d9c88b4add1)
#### Draw a circle in an image
```
import cv2
image = cv2.imread("iron.jpg")
image = cv2.resize(image, (400, 300))
height, width, _ = image.shape
center_coordinates = (width // 2, height // 2)
res = cv2.circle(image, center_coordinates, 120, (0, 255, 0), 10)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/3fbd11ac-4915-4f7a-be62-3268bc1ec7d7)

#### Add the text at the top-left corner of the image.
```
import cv2
image = cv2.imread("iron.jpg")
image = cv2.resize(image, (400, 300))
text = "Hey Jarvis"
position = (10, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255) 
thickness = 2
res = cv2.putText(image, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/3f2336bb-962e-4f74-973e-e14a49712f77)

### iii)Image Color Conversion
#### Convert the image from RGB to HSV and display it.
```
import cv2
image = cv2.imread('iron.jpg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
hsv = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/a95b2ba0-7fe6-4feb-9421-3f0cc475907f)
#### Convert the image from RGB to GRAY and display it.
```
import cv2
image = cv2.imread('iron.jpg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
gray = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/ec0f1013-e6d5-4049-9c42-ed7b9ba3e41b)
#### Convert the image from RGB to YCrCb and display it.
```
import cv2
image = cv2.imread('iron.jpg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
YCrCb = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/35e67052-975e-4d76-b5de-ea208670a865)
#### Convert the HSV image back to RGB and display it.
```
import cv2
image = cv2.imread('iron.jpg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
RGB = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',RGB)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/6bb90a43-503f-422f-8fc4-79e21de66158)
### iv)Access and Manipulate Image Pixels
```
import cv2
img = cv2.imread('iron.jpg', 1)
img = cv2.resize(img, (300, 200))
cv2.imshow('Original Image', img)
pixel_value = img[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
img[199, 199] = [255, 255, 255]  # Setting the pixel value to white (BGR)
cv2.imshow('Modified Image', img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/3d0f4833-ed38-4d2c-a639-113dbceb960d)
![image](https://github.com/user-attachments/assets/795c7a67-5dcd-454b-9c2d-b691d5369844)

### v)Image Resizing
```
import cv2
img = cv2.imread('iron.jpg', 1)
width=600
height=800
half_width=300
half_height=400
resized_img = cv2.resize(image, (300, 400))
cv2.imshow('Original',image)
cv2.imshow('resized',resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
![image](https://github.com/user-attachments/assets/0cb77af4-92e7-4add-a4ed-06a3f20ed906)

### vi)Image Cropping
```
import cv2
image1=cv2.imread('iron.jpg',1)
img1=cv2.resize(image1,(600,800))
x, y = 50, 50
width, height = 100, 100
roi = image1[y:y + height, x:x + width]
cv2.imshow('Cropped Image', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/15aa089b-4c2f-44a5-af92-2682c0f9ba7f)


### vii)Image Flipping
#### Flip the original image horizontally and display it
```
import cv2

img = cv2.imread("iron.jpg")
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_180)
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/e33aba1c-9172-4563-94cb-473a0ff0f4b9)

#### Flip the original image vertically and display it.
```
import cv2
img = cv2.imread("iron.jpg")
img1=cv2.resize(img,(600,800))
img = cv2.resize(img1,(300,200))
res=cv2.rotate(img,cv2.ROTATE_90_CLOCKWISE)
# Display the HSV image
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/72610e17-db5f-4809-a4cf-07ed7c04b73e)

### viii)Write and Save the Modified Image
```
import cv2
img = cv2.imread("iron.jpg")
img = cv2.resize(img,(300,200))
cv2.imwrite('IRON MAN.jpg',img)
```

![Untitled](https://github.com/user-attachments/assets/a7fbf92f-d6bb-4e0a-a19c-96b1174da4df)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







