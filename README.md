# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) Draw Shapes and Add Text.

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
1.  Draw a line from the top-left to the bottom-right of the image.

2.	Draw a circle at the center of the image.

3.	Draw a rectangle around a specific region of interest in the image.

4.	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
1.	Convert the image from RGB to HSV and display it.
2.	Convert the image from RGB to GRAY and display it.
3.	Convert the image from RGB to YCrCb and display it.
4.	Convert the HSV image back to RGB and display it.

### Step4:
1.	Access and print the value of the pixel at coordinates (100, 100).
2.	Modify the color of the pixel at (200, 200) to white.

### Step5:
Resize the original image to half its size and display it.
### Step6:
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
1.	Flip the original image horizontally and display it.
2.	Flip the original image vertically and display it.

### Step8:
Save the final modified image to your local directory.

## Program:
### Developed By: LISIANA T
### Register Number: 212222240053

## Output:

### 1. Read and display the image
i.Load an image from your local directory and display it.
```python
import cv2
image=cv2.imread('scenery.jpg',1)
image = cv2.resize(image, (400, 300))
cv2.imshow('DhariniPV_212222240024',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/75f70659-2624-4bb9-80cb-5cd76957d2fa)

### Draw Shapes and Add Text
(1) Draw a line from the top-left to the bottom-right of the image.
```python
import cv2
image = cv2.imread("scenery.jpg")
image = cv2.resize(image, (400, 300))
res = cv2.line(image, (0, 0), (image.shape[1], image.shape[0]), (255,0,0), 10)
cv2.imshow('DhariniPV_212222240024', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/f87a2f72-6904-4825-af30-071de0d85773)

2. Draw a circle at the center of the image.
```python
import cv2
image = cv2.imread("scenery.jpg")
image = cv2.resize(image, (400, 300))
height, width, _ = image.shape
center_coordinates = (width // 2, height // 2)
res = cv2.circle(image, center_coordinates, 120, (0, 255, 0), 10)
cv2.imshow('DhariniPV_212222240024', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/f70ab9fd-f586-4c03-9291-217a67e1b123)

3.Draw a rectangle around the full image.
```python
image = cv2.imread('Mountains.jpg') 
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
rectangle_img = cv2.rectangle(img_rgb, (0, 0), (300, 200), (255,0,0), 10)  # cv2.rectangle(image, start_point, end_point, color, thickness)
plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()
```
![image](https://github.com/user-attachments/assets/dcd7a8cd-7495-48d2-88f1-c289d739a33f)


4.Add the text "OpenCV Drawing" at the top-left corner of the image.
```python
import cv2
image = cv2.imread("scenery.jpg")
image = cv2.resize(image, (400, 300))
text = "OpenCV Drawing"
position = (10, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255) 
thickness = 2
res = cv2.putText(image, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
cv2.imshow('DhariniPV_212222240024', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/bb39bc06-25ea-4fd7-b9f6-16fdbc70fa2c)

### iii)Image Color Conversion
(i)Convert the image from RGB to HSV and display it
```python
import cv2
image = cv2.imread('scenery.jpg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
hsv = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/6f4e5be7-e075-4cb5-b87e-2de7c4f6392d)

(2) Convert the image from RGB to GRAY and display it.

```python
import cv2
image = cv2.imread('scenery.jpg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
gray = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/94ba15a5-b663-4d72-b244-354c370d993d)


(3) Convert the image from RGB to YCrCb and display it.
```python
import cv2
image = cv2.imread('scenery.jpg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
YCrCb = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/4248d46f-1aa8-4fde-99e4-fecec7034776)

(4) Convert the HSV image back to RGB and display it.
```python
import cv2
image = cv2.imread('scenery.jpg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
RGB = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',RGB)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/a6d2a64b-f87f-4a60-a57f-06213126af60)

### iv)Access and Manipulate Image Pixels
(1) Access and print the value of the pixel at coordinates (100, 100)
```python
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
```
![image](https://github.com/user-attachments/assets/5c4eb1f2-e481-4829-9ce1-ecda06bc4df4)

(2) Modify the color of the pixel at (200, 200) to white
```python
import cv2
image = cv2.imread('scenery.jpg',1)
image = cv2.resize(image,(400,300))
cv2.imshow('ORIGINAL IMAGE',image)
image[205:210, 205:210] = [255, 255, 255]
cv2.imshow('MODIFIED IMAGE', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/11a340c2-a55b-442b-85a2-400f3bfd4c67)

### v)Image Resizing:
Resize the original image to half its size and display it.
```python
cv2.imshow('ORIGINAL IMAGE',image)
resized_image = cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2))
cv2.imshow('RESIZED IMAGE', resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/2ea2e67e-575b-404f-8275-dbe56b323826)


### vi)Image Cropping
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```python
import cv2
image = cv2.imread('scenery.jpg',1)
image = cv2.resize(image,(400,300))
x, y = 50, 50
width, height = 100, 100
roi = image[y:y + height, x:x + width]
cv2.imshow('CROPPED IMAGE', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/42088f34-eab6-4f6a-9c49-60b4d72d369c)
### vii)Image Flipping:
(1) Flip the original image horizontally and display it.
```python
import cv2
image = cv2.imread("scenery.jpg")
image = cv2.resize(image,(300,200))
res=cv2.flip(image,1)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/299f4e37-e7b3-429d-8eed-38c2d3630bba)

(2) Flip the original image vertically and display it.
```python
import cv2
image = cv2.imread("scenery.jpg")
image = cv2.resize(image,(300,200))
res=cv2.flip(image,0)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/1caa763e-d7ce-427c-92c6-ad1d493a2dfb)


### viii)Write and Save the Modified Image
Save the final modified image to your local directory.
```python
import cv2
img = cv2.imread("scenery.jpg")
img = cv2.resize(img,(300,200))
cv2.imwrite('Mountains.jpg',img)
```
![image](https://github.com/user-attachments/assets/77cfd09b-aa53-49ff-85ce-61cdb3d03c31)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







