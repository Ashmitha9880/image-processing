# image-processing
1) develop a program to display gray scale image using read and write operations

import cv2<br>
img=cv2.imread("leaf1.jpg",0)<br>
cv2.imshow("image",img)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
**OUTPUT**

![image](https://user-images.githubusercontent.com/97940767/173810634-212154cc-7e46-4d7f-9bfe-edefafcdeb10.png)

2) DEVELOP A PROGRAM TO DISPLAY THE IMAGES USING matplotlib

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

(255, 255, 0)<br>
(255, 0, 0)<br>
(255, 192, 203)<br>

5)  Write a program to create image using color

from PIL import Image)<br>
img=Image.new("RGB",(200,400),(255,255,0)))<br>
img.show())<br>

**OUTPUT**
![image](https://user-images.githubusercontent.com/97940767/173814864-75f806a2-1fc0-4bb6-a8a8-93558b8810fe.png)

6) develop a program to visualize the image using various color space
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

7) DISPLAY THE IMAGE ATTRIBUTES

from PIL import Image<br>
image=Image.open("flower2.jpg")<br>
print("Filename:",image.filename)<br>
print("Format:",image.format)<br>
print("Mode:",image.mode)<br>
print("Size:",image.size)<br>
print("Width:",image.width)<br>
print("Height:",image.height)<br>
image.close()<br>

**OUTPUT**

![image](https://user-images.githubusercontent.com/97940767/173816249-af458bc1-284d-4501-9a79-76a7379d9827.png)

8) CONVERT THE ORIGINAL IMAGE TO GRAY SCALE AND THEN BINARY

import cv2<br><br>
img=cv2.imread('flower3.jpg')<br>
cv2.imshow("RGB",img)<br>
cv2.waitKey(0)<br>
#gray scale<br>
img=cv2.imread ('flower3.jpg',0)<br>
cv2.imshow("Gray",img)<br>
cv2.waitKey(0)<br>
#binary image<br>
ret,bw_img=cv2.threshold (img,127,255,cv2.THRESH_BINAR<br>Y)<br>
cv2.imshow("Binary",bw_img)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>

**OUTPUT**

![image](https://user-images.githubusercontent.com/97940767/174045981-050582dd-c5e9-45d4-8744-2243618d2aaf.png)
![image](https://user-images.githubusercontent.com/97940767/174046144-88b37482-f474-4be1-a526-29e3da998016.png)
![image](https://user-images.githubusercontent.com/97940767/174046296-0fe3f818-5453-4d09-8ebd-f235c247bc35.png)

9) RESIZE THE ORIGINAL IMAGES

import cv2<br>
img=cv2.imread('flower1.jpg')<br>
print('original image length width',img.shape)<br>
cv2.imshow('original image',img)<br>
cv2.waitKey(0)<br>
#to show the resized image<br>
imgresize=cv2.resize(img,(150,160))<br>
cv2.imshow('Resized image',imgresize)<br>
print('resized image lenght width',imgresize.shape)<br>
cv2.waitKey(0)<br>

**OUTPUT**
![image](https://user-images.githubusercontent.com/97940767/174047733-01ac6e5c-d14e-4c3d-95c6-297ff947ef0c.png)<br>

![image](https://user-images.githubusercontent.com/97940767/174048151-a9493847-3382-4d88-9540-04fd81b7f472.png)<br>
![image](https://user-images.githubusercontent.com/97940767/174048317-81573d9e-2a9b-4b53-84a1-0325854557ac.png)<br>


**Lab exercise:**

1. Develop a program to readimage using URL.<br>
from skimage import io<br>
import matplotlib.pyplot as plt<br>
url='https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS0XJ2Kil6XedNVlxv9wMqE6dZJ7VF1DcFcow&usqp=CAU'<br>
image=io.imread(url)<br>
plt.imshow(image)<br>
plt.show()<br>

**OUTPUT**

![image](https://user-images.githubusercontent.com/97940767/175004887-6c735fdd-6cbe-4e1e-9208-4f1b1e68423d.png)


**2. Write a program to mask and blur the image**

import cv2<br>
import matplotlib.image as mping<br>
import matplotlib.pyplot as plt<br>
img=cv2.imread('fish2.jpg')<br>
plt.imshow(img)<br>
plt.show()<br>

OUTPUT
![image](https://user-images.githubusercontent.com/97940767/175014872-eab018f1-80bf-4fd8-b749-d7d1f391dcbe.png)<br>

hsv_img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)<br>
light_orange=(1,190,200)<br>
dark_orange=(18,255,255)<br>
mask=cv2.inRange(img,light_orange,dark_orange)<br>
result=cv2.bitwise_and(img,img,mask=mask)<br>
plt.subplot(1,2,1)<br>
plt.imshow(mask,cmap="gray")<br>
plt.subplot(1,2,2)<br>
plt.imshow(result)<br>
plt.show()<br>

**OUTPUT**<br>
![image](https://user-images.githubusercontent.com/97940767/175015021-62cf3b7f-fdec-411e-bcc0-f2e930f6393c.png)<br>

light_white=(0,0,200)<br>
dark_white=(145,60,255)<br><br>
mask_white=cv2.inRange(hsv_img,light_white,dark_white)<br>
result_white=cv2.bitwise_and(img,img,mask=mask_white)<br>
plt.subplot(1,2,1)<br>
plt.imshow(mask_white,cmap="gray")<br>
plt.subplot(1,2,2)<br>
plt.imshow(result_white)<br>
plt.show()<br>

**OUTPUT**<br>
![image](https://user-images.githubusercontent.com/97940767/175015216-8c572cf1-2f25-460c-910f-237f28e122cd.png)<br>

final_mask=mask+mask_white<br>
final_result=cv2.bitwise_and(img,img,mask=final_mask)<br>
plt.subplot(1,2,1)<br>
plt.imshow(final_mask,cmap="gray")<br>
plt.subplot(1,2,2)<br>
plt.imshow(final_result)<br>
plt.show()<br>

**OUTPUT**<br>
![image](https://user-images.githubusercontent.com/97940767/175015425-e0fc3440-e479-46c7-8fd5-01ef2c078749.png)<br>

blur=cv2.GaussianBlur(final_result,(7,7),0)<br>
plt.imshow(blur)<br>
plt.show()<br>

**OUTPUT**<br>
![image](https://user-images.githubusercontent.com/97940767/175015589-71a69b0c-f27e-41aa-a2a6-89ba32dd3e3d.png)<br>

**3. Write a program to perform arithmatic operations on images**

import cv2<br>
import matplotlib.image as mping<br>
import matplotlib.pyplot as plt<br>

img1=cv2.imread('f1.jpg')<br>
img2=cv2.imread('f2.jpg')<br>

fimg1=img1+img2<br>
plt.imshow(fimg1)<br>
plt.show()<br>

cv2.imwrite('output.jpg',fimg1)<br>
fimg2=img1-img2<br>
plt.imshow(fimg2)<br>
plt.show()<br>


cv2.imwrite('output.jpg',fimg2)<br>
fimg3=img1*img2<br>
plt.imshow(fimg3)<br>
plt.show()<br>

cv2.imwrite('output.jpg',fimg3)<br>
fimg4=img1/img2<br>
plt.imshow(fimg4)<br>
plt.show()<br>


cv2.imwrite('output.jpg',fimg4)<br><br>

**OUTPUT**<br>

![image](https://user-images.githubusercontent.com/97940767/175022012-4c02ec53-f7d6-4e6e-ab67-1b0350bac464.png)<br>
![image](https://user-images.githubusercontent.com/97940767/175022095-7c368bd0-d762-4154-a6d8-ab3ec92b7948.png)<br>

4.  Develop the program to change the image to different color spaces<br>

import cv2<br>
img=cv2.imread ('E:\\f1.jpg')<br>
gray=cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)<br>
hsv=cv2.cvtColor(img,cv2.COLOR_BGR2HSV)<br>
lab=cv2.cvtColor(img,cv2.COLOR_BGR2LAB)<br>
hls=cv2.cvtColor(img,cv2.COLOR_BGR2HLS)<br>
yuv=cv2.cvtColor(img,cv2.COLOR_BGR2YUV)<br>
cv2.imshow("GRAY image",gray)<br>
cv2.imshow("HSV image",hsv)<br>
cv2.imshow("LAB image",lab)<br>
cv2.imshow("HLS image",hls)<br>
cv2.imshow("YUV image",yuv)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>

**OUTPUT**<br>

![image](https://user-images.githubusercontent.com/97940767/175273467-13f59c7f-ce21-470c-abad-a8d9cac0bc40.png)
![image](https://user-images.githubusercontent.com/97940767/175273544-aed46d3e-e9af-4c68-a675-069b5f7ff5c3.png)
![image](https://user-images.githubusercontent.com/97940767/175273678-7fd79d49-679d-44d9-9c80-675f407e7d59.png)
![image](https://user-images.githubusercontent.com/97940767/175273887-e2526e1f-bf37-43c9-baf4-8870db0ea739.png)
![image](https://user-images.githubusercontent.com/97940767/175273973-07ada23c-e35d-46d6-88ab-b3f5ffa6031e.png)


5 program to create an array using 2d array

import cv2 as c<br>
import numpy  as np<br>
from PIL import Image<br>
array = np.zeros([100,200,3],dtype=np.uint8)<br>
array[:,:100]=[255,130,0]<br>
array[:,100:]=[0,0,255]<br>
img=Image.fromarray(array)<br>
img.save('image1.png')<br>
img.show()<br>
c.waitKey(0)<br>

**OUTPUT**<br>

![image](https://user-images.githubusercontent.com/97940767/175280905-2d59a26f-c39a-4fd1-8a14-8776a7e65031.png)<br>

