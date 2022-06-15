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
