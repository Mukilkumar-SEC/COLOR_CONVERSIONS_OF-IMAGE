# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By: MUKIL KUMAR V
### Register Number: 212222230087


## Output:

### i) Read and display the image
```py
    import cv2
    image=cv2.imread('images.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('natural',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
## Output:

![Screenshot 2024-09-16 152149](https://github.com/user-attachments/assets/ab3dec3b-44e9-4377-b2b2-1458196bce08)


### ii)Write the image
```py
    import cv2
    image=cv2.imread('images.jpg',0)
    cv2.imwrite('natural.jpg',image)
```
## Output:

![write the image](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/9d717855-bb9d-41e6-916f-ac3205453f25)

### iii)Shape of the Image
```py
    import cv2
    image=cv2.imread('images.jpg',1)
    print(image.shape)
```
## Output:
![shape the image](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/46902cb3-9d2f-4729-98a7-b9e04fc95ca2)

### iv)Access rows and columns
```py
    import random
    import cv2
    image=cv2.imread('images.jpg',1)
    image=cv2.resize(image,(400,400))
    for i in range (150,200):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('natural',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-09-16 153051](https://github.com/user-attachments/assets/23ba8654-94c3-4132-832e-7be79ecd6a6a)



### v)Cut and paste portion of image
```py
   import cv2
   image=cv2.imread('images.jpg',1)
   image=cv2.resize(image,(400,400))
   tag =image[130:200,110:190]
   image[110:180,120:200] = tag
   cv2.imshow('natural',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()
```
## Output:
![image](https://github.com/user-attachments/assets/562a016e-f778-416b-a774-a8c0269dfaa8)


### vi) BGR and RGB to HSV and GRAY
```py
import cv2
img = cv2.imread('images.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![image](https://github.com/user-attachments/assets/8bdd720c-2257-4d19-8dd3-6a8685a69156)


### vii) HSV to RGB and BGR
```py
import cv2
img = cv2.imread('images.jpg')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)
RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![image](https://github.com/user-attachments/assets/5c5724bc-ce84-41c5-9e3f-d04e28b376c1)





### viii) RGB and BGR to YCrCb
```py
import cv2
img = cv2.imread('images.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:


![image](https://github.com/user-attachments/assets/de4aa789-d519-495f-aecb-2ce181a26768)




### ix) Split and merge RGB Image
```py
import cv2
img = cv2.imread('images.jpg',1)
img = cv2.resize(img,(300,200))
R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]
cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)
merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:


![image](https://github.com/user-attachments/assets/c91482a2-70a7-401f-a4ed-ff35a0e2e0ec)




### x) Split and merge HSV Image
```py
import cv2
img = cv2.imread("images.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
H,S,V=cv2.split(img)
cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)
merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![image](https://github.com/user-attachments/assets/f686fd34-9363-44f4-961b-abf75fb93637)




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.
