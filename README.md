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
## Output:
### i)Image Translation


![download](https://user-images.githubusercontent.com/118707669/231389498-1f0e5252-ad8f-4738-b4d3-1ca56139245f.png)


![download](https://user-images.githubusercontent.com/118707669/231389546-da9fed2c-7af0-42c4-a8ad-f23090d36b0a.png)

### ii) Image Scaling
![download](https://user-images.githubusercontent.com/118707669/231389582-9b448a0b-ff9b-4246-9622-41765585f8f4.png)



### iii)Image shearing



![download](https://user-images.githubusercontent.com/118707669/231393021-ac66b322-e58f-460b-a402-dc20a6f2c318.png)
![download](https://user-images.githubusercontent.com/118707669/231393068-bca86e73-c6d5-49af-9850-2fb14e49f35b.png)

### iv)Image Reflection
![download](https://user-images.githubusercontent.com/118707669/231393105-17381a21-89f6-451b-97df-d4529d00f14a.png)


![download](https://user-images.githubusercontent.com/118707669/231393120-90609daa-2ec4-4023-bb79-7df84d3f19f0.png)


### v)Image Rotation

![download](https://user-images.githubusercontent.com/118707669/231390551-f14e29cf-2bef-4734-883f-c2c292972c8e.png)


### vi)Image Cropping

![download](https://user-images.githubusercontent.com/118707669/231390300-1903eefa-00b7-4f45-85d3-30c363307f56.png)





## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
