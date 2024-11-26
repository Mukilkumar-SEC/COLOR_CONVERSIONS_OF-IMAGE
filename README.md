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
1.Draw a line from the top-left to the bottom-right of the image.

2.Draw a circle at the center of the image.

3.Draw a rectangle around a specific region of interest in the image.

4.Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
1.Convert the image from RGB to HSV and display it.

2.Convert the image from RGB to GRAY and display it.

3.Convert the image from RGB to YCrCb and display it.

4.Convert the HSV image back to RGB and display it.

### Step4:
1.Access and print the value of the pixel at coordinates (100, 100).

2.Modify the color of the pixel at (200, 200) to white.

### Step5:
Resize the original image to half its size and display it.
### Step6:
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
1.Flip the original image horizontally and display it.

2.Flip the original image vertically and display it.

### Step8:
Save the final modified image to your local directory.


## Program:
### Developed By:Mukil kumar v
### Register Number: 212222230087


## Output:

### i)Read and Display an Image
i)Load an image from your local directory and display it.
```
import cv2
image=cv2.imread('vijay.webp',1)
image = cv2.resize(image, (400, 300))
cv2.imshow('Renuga_212222230118',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-24 181401](https://github.com/user-attachments/assets/77ba3fd7-bbff-4646-be3b-b288dc30da72)

### ii)Draw Shapes and Add Text
1. Draw a line from the top-left to the bottom-right of the image.
```
import cv2
image = cv2.imread("vijay.webp")
image = cv2.resize(image, (400, 300))
res = cv2.line(image, (0, 0), (image.shape[1], image.shape[0]), (255,0,0), 10)
cv2.imshow('Renuga_212222230118', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-24 181534](https://github.com/user-attachments/assets/c41ee607-6bd7-43af-8437-95f84478d564)

2.Draw a circle at the center of the image.
```
import cv2
image = cv2.imread("vijay.webp")
image = cv2.resize(image, (400, 300))
height, width, _ = image.shape
center_coordinates = (width // 2, height // 2)
res = cv2.circle(image, center_coordinates, 120, (0, 255, 0), 10)
cv2.imshow('Renuga_212222230118', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-24 181651](https://github.com/user-attachments/assets/ec674bae-cebb-4b87-8415-a9313c9e3797)

3.Draw a rectangle around a specific region of interest in the image.
```
import cv2
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('vijay.webp')

# Check if the image is loaded
if image is None:
    print("Error: Image not found or failed to load.")
else:
    # Convert BGR to RGB
    img_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

    # Draw a rectangle on the image
    rectangle_img = cv2.rectangle(img_rgb, (0, 0), (300, 200), (255, 0, 0), 10)  # Blue rectangle

    # Display the image with the rectangle
    plt.imshow(rectangle_img)
    plt.title("Image with Rectangle")
    plt.axis('off')
    plt.show()
```
![Screenshot 2024-11-24 151035](https://github.com/user-attachments/assets/db8505bd-1382-4950-9c77-94835c19bb2b)





4.Add the text "OpenCV Drawing" at the top-left corner of the image.
```
import cv2
image = cv2.imread("vijay.webp")
image = cv2.resize(image, (400, 300))
text = "OpenCV Drawing"
position = (10, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255) 
thickness = 2
res = cv2.putText(image, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
cv2.imshow('Renuga_212222230118', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-24 181939](https://github.com/user-attachments/assets/d7053f9d-84bb-4f15-9fc8-a0f183f585fe)

### iii)Image Color Conversion
1.Convert the image from RGB to HSV and display it.
```
import cv2
image = cv2.imread('vijay.webp',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
hsv = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-24 182105](https://github.com/user-attachments/assets/5c627e49-4606-4c6a-8579-152dd3a40ff4)

2.Convert the image from RGB to GRAY and display it.
```
import cv2
image = cv2.imread('vijay.webp',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
gray = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-24 182215](https://github.com/user-attachments/assets/4e9b18d8-0d0b-4a7d-9a36-04934dff064e)

3.Convert the image from RGB to YCrCb and display it.
```
import cv2
image = cv2.imread('vijay.webp',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
YCrCb = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-24 182309](https://github.com/user-attachments/assets/b75ad013-cd0a-4212-8679-c60c842f2045)

4.Convert the HSV image back to RGB and display it.
```
import cv2
image = cv2.imread('vijay.webp',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
RGB = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',RGB)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-24 182357](https://github.com/user-attachments/assets/8c42da8b-8c56-4d89-bcdc-88c09f294b39)

### iv)Access and Manipulate Image Pixels

1.Access and print the value of the pixel at coordinates (100, 100)
```
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
```
![Screenshot 2024-09-24 183254](https://github.com/user-attachments/assets/126e00b4-3e5b-4799-b291-ef581d3babf6)

2.Modify the color of the pixel at (200, 200) to white.
```
import cv2
image = cv2.imread('vijay.webp',1)
image = cv2.resize(image,(400,300))
cv2.imshow('ORIGINAL IMAGE',image)
image[205:210, 205:210] = [255, 255, 255]
cv2.imshow('MODIFIED IMAGE', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-24 182535](https://github.com/user-attachments/assets/3add0b5b-1d28-44c4-b6c8-e2a549fa1769)

### v)Image Resizing
Resize the original image to half its size and display it.
```
cv2.imshow('ORIGINAL IMAGE',image)
resized_image = cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2))
cv2.imshow('RESIZED IMAGE', resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-24 182636](https://github.com/user-attachments/assets/ae09b436-4cda-4fe7-964e-21cdb22078ce)

### vi)Image Cropping
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```
import cv2
image = cv2.imread('vijay.webp',1)
image = cv2.resize(image,(400,300))
x, y = 50, 50
width, height = 100, 100
roi = image[y:y + height, x:x + width]
cv2.imshow('CROPPED IMAGE', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-24 182804](https://github.com/user-attachments/assets/e9c8f6ef-c177-41d7-b94f-dbd6172e51c6)

### vii)Image Flipping
1.Flip the original image horizontally and display it.
```
import cv2
image = cv2.imread("vijay.webp")
image = cv2.resize(image,(300,200))
res=cv2.flip(image,1)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-24 182850](https://github.com/user-attachments/assets/228fce4b-9ebe-47cb-99b7-6e976702e902)

2. Flip the original image vertically and display it.
```
import cv2
image = cv2.imread("vijay.webp")
image = cv2.resize(image,(300,200))
res=cv2.flip(image,0)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-24 183046](https://github.com/user-attachments/assets/f7d39d46-394f-49a6-8da0-6eb7d9f314ba)

### viii)Write and Save the Modified Image
Save the final modified image to your local directory.
```
import cv2
img = cv2.imread("vijay.webp")
img = cv2.resize(img,(300,300))
cv2.imwrite('ajith.webp',img)
```
![Screenshot 2024-09-24 183830](https://github.com/user-attachments/assets/4ddefaa6-373f-43fc-8bbf-45b01f0d2c50)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







