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
### Developed By: P Balasudhan
### Register Number: 212222240017

## Output:

### i)Read and Display an Image
```
import cv2
img=cv2.imread('str.jpg')
cv2.imshow('STR',img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-19 160851](https://github.com/user-attachments/assets/e3d6dcd6-dbc6-44d8-8013-fa448989d360)

<br>
<br>

### ii)Draw Shapes and Add Text
i)Draw a line from the top-left to the bottom-right of the image.
```
import cv2
img = cv2.imread("str.jpg")
res = cv2.line(img, (0, 0), (1025, 680), (255, 0, 0), 3)
cv2.imshow('STR', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-19 160950](https://github.com/user-attachments/assets/d8f96b61-0c4e-48f2-ae58-4e5776fc2d49)

ii)Draw a circle at the center of the image.
```
# Load the image
img = cv2.imread("str.jpg")

# Get the dimensions of the image
height, width, _ = img.shape

# Calculate the center of the image
center_coordinates = (width // 2, height // 2)

# Draw a circle at the center of the image
res = cv2.circle(img, center_coordinates, 150, (0, 0, 255), 10)

# Display the image with the circle
cv2.imshow('str', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-19 161057](https://github.com/user-attachments/assets/693b625e-1d61-40d4-9d24-b070d4468e54)

iii)Draw a rectangle around a specific region of interest in the image.
```
img = cv2.imread("str.jpg")
start=(0,0)
stop=(318,200)
color=(255,255,100)
thickness=10
res_img=cv2.rectangle(img,start,stop,color,thickness)
# Display the HSV image
cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-19 161130](https://github.com/user-attachments/assets/884faf42-237e-4417-ae1f-641f9147778e)


iv)Add the text at the bottom of the image.
```
img = cv2.imread("str.JPG")

# Define the text to be added and its position
text = "ORU COWW..."
position = (140, 300)  # Positioning the text at the top-left corner

# Set the font, scale, color, and thickness of the text
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255)  # White color
thickness = 2

# Add the text to the image
res = cv2.putText(img, text, position, font, font_scale, color, thickness, cv2.LINE_AA)

# Display the image with the text
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-19 161402](https://github.com/user-attachments/assets/1739d396-ffa8-4085-8731-59ce752dd324)
<br>
<br>

### iii)Image Color Conversion
i)Convert the image from RGB to HSV and display it.
```
cv2.imshow('Original Image',img)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-19 161449](https://github.com/user-attachments/assets/2de7d79d-6c41-43eb-82f3-74d41e509498)

ii.)Convert the image from RGB to GRAY and display it.
```
cv2.imshow('Original Image',img)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-19 161529](https://github.com/user-attachments/assets/fddc9c41-5f02-402e-8ace-50e1124ee710)


iii.)Convert the image from RGB to YCrCb and display it.
```
cv2.imshow('Original Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-19 161559](https://github.com/user-attachments/assets/f7f6ee35-8803-4e85-81e2-f9de22fba1b5)


iv.)Convert the HSV image back to RGB and display it.
```
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-19 161626](https://github.com/user-attachments/assets/b6d43813-fb9d-4d4d-86d2-103c846395c0)

<br>
<br>

### iv)Access and Manipulate Image Pixels
```
# Show the original image
cv2.imshow('Original Image', img)

# 1. Access and print the value of the pixel at coordinates (100, 100)
pixel_value = img[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")

# 2. Modify the color of the pixel at (199, 199) to white
img[199, 199] = [255, 255, 255]  # Setting the pixel value to white (BGR)

# Display the modified image
cv2.imshow('Modified Image', img)

# Wait for a key press and close the windows
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-19 161743](https://github.com/user-attachments/assets/2e71b61c-187f-4dcc-ae80-a0696817f313)

<br>
<br>

### v)Image Resizing
```
width=600
height=800
half_width=300
half_height=400
resized_img = cv2.resize(img, (300, 400))
cv2.imshow('Original',img)
cv2.imshow('resized',resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-19 161812](https://github.com/user-attachments/assets/46e8ae20-b59c-4dff-bd1b-bf90569ac0e0)

<br>
<br>

### vi)Image Cropping
```
# Define the starting point and size of the ROI
x, y = 50, 50
width, height = 150, 150

# Crop the ROI
roi = img[y:y + height, x:x + width]

# Display the cropped ROI
cv2.imshow('Cropped Image', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-19 161950](https://github.com/user-attachments/assets/9b1f330c-15f3-4e5b-a208-256e9abc2756)

<br>
<br>

### vii)Image Flipping
i.)Flip the original image horizontally and display it.
```
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_180)
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-19 162013](https://github.com/user-attachments/assets/4c50e8c1-3632-41b8-8ecf-fd13041fa25c)


ii.)Flip the original image vertically and display it.
```
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_90_CLOCKWISE)
# Display the HSV image
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-09-19 162034](https://github.com/user-attachments/assets/20bcc71f-88f1-40dc-8170-23a59e8cd155)

<br>
<br>

### viii)Write and Save the Modified Image
```
cv2.imwrite('str.jpg',img)
```
### OUTPUT:
![Screenshot 2024-09-19 211129](https://github.com/user-attachments/assets/91d81fdd-1b78-4ec3-9073-04e1c8b27f4f)

<br>
<br>

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.
