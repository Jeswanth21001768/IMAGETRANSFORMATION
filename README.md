# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation, and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries read the original image and save it as an image variable.

### Step2:
Translate the image

### Step3:
Scale the image.

### Step4:
Shear the image.

### Step5:
Make a Reflection on the image.

### Step6:
Rotate the image


## Program:
```
Developed By: Jeswanth S
Register Number:212221230042

i)Original Image:
# To show the original image and to find the shape of the image
import cv2
import numpy as np
img = cv2.imread('prof.jpg',-1)
original = cv2.cvtColor(img , cv2.COLOR_BGR2RGB)
cv2.imshow('input',original)
cv2.waitKey(0)
cv2.destroyAllWindows()
original.shape
row, col, dim =original.shape

ii)Image Translation

translation = np.float32([[1,0,100],[0,1,150],[0,0,1]])
translated_image = cv2.warpPerspective(original,translation,(col,row))
cv2.imshow('translated_image',translated_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

iii)Image shearing

shear_x = np.float32([[1,0.7,0],[0,1,0],[0,0,1]])
shear_y = np.float32([[1,0,0],[0.3,1,0],[0,0,1]])
sheared_x= cv2.warpPerspective(original,shear_x,(col,row))
sheared_y = cv2.warpPerspective(original,shear_y,(col,row))
cv2.imshow('shear_x',sheared_x)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.imshow('shear_y',sheared_y)
cv2.waitKey(0)
cv2.destroyAllWindows()



iv)Image Reflection

ref_x = np.float32([[1,0,0],[0,-1,row],[0,0,1]])
ref_y = np.float32([[-1,0,col],[0,1,0],[0,0,1]])
reflect_x= cv2.warpPerspective(original,ref_x,(col,row))
reflect_y = cv2.warpPerspective(original,ref_y,(col,row))
cv2.imshow('reflected_x',reflect_x)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.imshow('reflected_y',reflect_y)
cv2.waitKey(0)
cv2.destroyAllWindows()

v)Image Rotation

angle = np.radians(15)
mat_rotate = np.float32([[np.cos(angle),-
(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotate_img =cv2.warpPerspective(original,mat_rotate,(col,row))
cv2.imshow('rotated',rotate_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

vi)Image Cropping

cropped_img=img[10:500,25:600] 
cv2.imshow('after_cropping',cropped_img);
cv2.waitKey(0)
cv2.destroyAllWindows()


```
## Output:
### i)Image Translation
![image](https://github.com/Jeswanth21001768/IMAGETRANSFORMATION/assets/94155480/b347405b-4e3c-436f-928c-cd4000b4fec6)
### ii) Image Scaling
![image](https://github.com/Jeswanth21001768/IMAGETRANSFORMATION/assets/94155480/0b0d8ad9-9e21-4db7-a702-996b044effa6)
### iii)Image shearing
![image](https://github.com/Jeswanth21001768/IMAGETRANSFORMATION/assets/94155480/84c99cdd-817f-4daf-b184-4d4143436158)
![image](https://github.com/Jeswanth21001768/IMAGETRANSFORMATION/assets/94155480/fea2f5a8-b234-4f4f-85d3-5836a839db89)
### iv)Image Reflection
![image](https://github.com/Jeswanth21001768/IMAGETRANSFORMATION/assets/94155480/1ef0b7ba-519b-469b-a582-81391571b207)
![image](https://github.com/Jeswanth21001768/IMAGETRANSFORMATION/assets/94155480/17bb1f26-42b8-4c5c-9d3c-478b94c043cb)
### v)Image Rotation
![image](https://github.com/Jeswanth21001768/IMAGETRANSFORMATION/assets/94155480/fb3aef37-e618-43c0-8807-7dfcdcd993c3)
### vi)Image Cropping
![image](https://github.com/Jeswanth21001768/IMAGETRANSFORMATION/assets/94155480/0e1909b0-1f77-451f-94f2-a802b18c3ac4)

## Result: 
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation, and Cropping are done using OpenCV and Python programming.
