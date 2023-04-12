# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image using
M=np.float32([[1,0,20],[0,1,50],[0,0,1]])
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step3:
Scale the image using
M=np.float32([[1.5,0,0],[0,2,0],[0,0,1]])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step4:
Shear the image using
M_x=np.float32([[1,0.2,0],[0,1,0],[0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))

### Step5:
Reflection of image can be achieved through the code
M_x=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
### Step 6:
Rotate the image using
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step 7:
Crop the image using
cropped_img=input_img[20:150,60:230]

### Step 8:
Display all the Transformed images.

## Program:
```python
Developed By: Marella Dharanesh
Register Number:212222240062
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("img.jpg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape

i)Image Translation
M=np.float32([[1,0,20],
             [0,1,50],
             [0,0,1]])
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_img)
plt.show()

ii) Image Scaling
M=np.float32([[1.5,0,0],
             [0,2,0],
             [0,0,1]])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()

iii)Image shearing
M_x=np.float32([[1,0.2,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1,0,0],
               [0.4,1,0],
               [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()


iv)Image Reflection
M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()



v)Image Rotation
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()




vi)Image Cropping
cropped_img=input_img[20:150,60:230]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()




```

### i)Image Translation

## Output:


![download](https://user-images.githubusercontent.com/118707669/231393735-4f826915-716d-408d-9b55-05b250239777.png)



![download](https://user-images.githubusercontent.com/118707669/231393824-e2abf53d-3c9c-4fb5-a9b5-dafb70f0ea4c.png)











### ii) Image Scaling
![download](https://user-images.githubusercontent.com/118707669/231393931-fb471382-d718-47cd-b884-a4a58ff5e044.png)



### iii)Image shearing
![download](https://user-images.githubusercontent.com/118707669/231393983-ea6c40cf-73a4-4e49-9271-89f38888ccbf.png)


![download](https://user-images.githubusercontent.com/118707669/231394001-efd82b9e-a1e5-4fdf-b849-71f5a9837e61.png)



### iv)Image Reflection
![download](https://user-images.githubusercontent.com/118707669/231393105-17381a21-89f6-451b-97df-d4529d00f14a.png)


![download](https://user-images.githubusercontent.com/118707669/231393120-90609daa-2ec4-4023-bb79-7df84d3f19f0.png)


### v)Image Rotation

![download](https://user-images.githubusercontent.com/118707669/231393678-50d3fb99-01bb-4110-a3f4-6052eb66fa8e.png)


### vi)Image Cropping



![download](https://user-images.githubusercontent.com/118707669/231393647-07f9f23e-8214-49d0-8edf-a5ccef5f94fe.png)



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
