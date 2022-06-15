# image-processing
1) develop a program to display gray scale image using read and write operations

import cv2<br>
img=cv2.imread("leaf1.jpg",0)<br>
cv2.imshow("image",img)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
**OUTPUT**

![image](https://user-images.githubusercontent.com/97940767/173810634-212154cc-7e46-4d7f-9bfe-edefafcdeb10.png)

2)DEVELOP A PROGRAM TO DISPLAY THE IMAGES USING matplotlib

import matplotlib.image as mping<br>
import matplotlib.pyplot as plt<br>
img=mping.imread("flower1.jpg")<br>
plt.imshow(img)<br>

**OUTPUT**

![image](https://user-images.githubusercontent.com/97940767/173811814-c62c4548-f8c3-422d-98a6-c83aee611109.png)

3) develop a program to perform linear transformation rotation
from PIL import Image<br>
img=Image.open("plant1.jpg")<br>
img=img.rotate(180)<br>
img.show()<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>

**OUTPUT**


![image](https://user-images.githubusercontent.com/97940767/173813160-ccca0a77-63ad-4ebc-b46d-f2f4dd6f3487.png)

4) DEVELOP PROGRAM TO CONVERT colorstring to RGB COLOR VALUES

import cv2<br>
from PIL import ImageColor<br>
img1=ImageColor.getrgb("yellow")<br>
print(img1)<br>
img1=ImageColor.getrgb("red")<br>
print(img1)<br>
img1=ImageColor.getrgb("pink")<br>
print(img1)<br>

**OUTPUT**

(255, 255, 0)
(255, 0, 0)
(255, 192, 203)

5)Write a program to create image using color

from PIL import Image)<br>
img=Image.new("RGB",(200,400),(255,255,0)))<br>
img.show())<br>

**OUTPUT**
![image](https://user-images.githubusercontent.com/97940767/173814864-75f806a2-1fc0-4bb6-a8a8-93558b8810fe.png)

6)develop a program to visualize the image using various color space
import cv2<br>
import matplotlib.pyplot as plt<br>
import numpy as np<br>
img=cv2.imread("butterfly1.jpg")<br>
plt.imshow(img)<br>
plt.show()<br>
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)<br>
plt.imshow(img)<br>
plt.show()<br>
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)<br>
plt.imshow(img)<br>
plt.show()<br>
**OUTPUT**

![image](https://user-images.githubusercontent.com/97940767/173815223-fbee911c-47c8-4977-a058-6d41daf3c914.png)

7)DISPLAY THE IMAGE ATTRIBUTES

from PIL import Image<br>
image=Image.open("flower2.jpg")<br>
print("Filename:",image.filename)<br>
print("Format:",image.format<br>)
print("Mode:",image.mode)<br>
print("Size:",image.size)<br>
print("Width:",image.width)<br>
print("Height:",image.height)<br>
image.close()<br>

**OUTPUT**

![image](https://user-images.githubusercontent.com/97940767/173816249-af458bc1-284d-4501-9a79-76a7379d9827.png)



