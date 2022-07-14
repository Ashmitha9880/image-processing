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

10. Develop a program to readimage using URL.<br>
from skimage import io<br>
import matplotlib.pyplot as plt<br>
url='https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS0XJ2Kil6XedNVlxv9wMqE6dZJ7VF1DcFcow&usqp=CAU'<br>
image=io.imread(url)<br>
plt.imshow(image)<br>
plt.show()<br>

**OUTPUT**

![image](https://user-images.githubusercontent.com/97940767/175004887-6c735fdd-6cbe-4e1e-9208-4f1b1e68423d.png)


**11. Write a program to mask and blur the image**

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

**12. Write a program to perform arithmatic operations on images**

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

**13.  Develop the program to change the image to different color spaces<br>
**
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

14.create an image using 2d array

import cv2 as c<br>
import numpy  as np<br>
from PIL import Image
array = np.zeros([100,200,3],dtype=np.uint8)<br>
array[:,:100]=[255,130,0]<br>
array[:,100:]=[0,0,255]<br>
img=Image.fromarray(array)<br>
img.save('image1.png')<br>
img.show()<br>
c.waitKey(0)<br>

**OUTPUT**<br><br>

![image](https://user-images.githubusercontent.com/97940767/175285630-3320a3f6-671c-40d8-be9a-e1709e265c06.png)

**15.develop image using bitwise operations**<br>
import cv2<br>
import matplotlib.pyplot as plt<br>
image1=cv2.imread('b2.jpg',1)<br>
image2=cv2.imread('b2.jpg')<br>
ax=plt.subplots(figsize=(15,10))
bitwiseAnd=cv2.bitwise_and(image1,image2)<br>
bitwiseOr=cv2.bitwise_or(image1,image2)<br>
bitwiseXor=cv2.bitwise_xor(image1,image2)<br>
bitwiseNot_img1=cv2.bitwise_not(image1,image2)<br>
bitwiseNot_img2=cv2.bitwise_not(image1,image2)<br>
plt.subplot(151)<br>
plt.imshow(bitwiseAnd)<br>
plt.subplot(152)<br>
plt.imshow(bitwiseOr)<br>
plt.subplot(153)<br>
plt.imshow(bitwiseXor)<br>
plt.subplot(154)<br>
plt.imshow(bitwiseNot_img1)<br>
plt.subplot(155)<br>
plt.imshow(bitwiseNot_img2)<br>
cv2.waitKey(0)<br><br>

**OUTPUT**<br>

![image](https://user-images.githubusercontent.com/97940767/176403223-0c9905fc-99fa-4fbf-87a5-b0fa7ca4056f.png)

import cv2<br>
import matplotlib.pyplot as plt<br>
image1=cv2.imread('a1.jpg',1)<br>
image2=cv2.imread('a2.jpg')<br>
ax=plt.subplots(figsize=(15,10))<br>
bitwiseAnd=cv2.bitwise_and(image1,image2)<br>
bitwiseOr=cv2.bitwise_or(image1,image2)<br>
bitwiseXor=cv2.bitwise_xor(image1,image2)<br>
bitwiseNot_img1=cv2.bitwise_not(image1)<br>
bitwiseNot_img2=cv2.bitwise_not(image2)<br>
plt.subplot(151)<br>
plt.imshow(bitwiseAnd)<br>
plt.subplot(152)<br>
plt.imshow(bitwiseOr)<br>
plt.subplot(153)<br>
plt.imshow(bitwiseXor)<br>
plt.subplot(154)<br>
plt.imshow(bitwiseNot_img1)<br>
plt.subplot(155)<br>
plt.imshow(bitwiseNot_img2)<br>
cv2.waitKey(0)<br>

**OUTPUT**<br>

![image](https://user-images.githubusercontent.com/97940767/176406746-fe22eb09-f71e-430e-922d-b95861898d01.png)

**16.develop image using blurring**

import cv2<br>
import numpy as np<br>

image=cv2.imread('z2.jpg')<br>
cv2.imshow('original image',image) <br>
cv2.waitKey(0)

#gaussian blur<br>

Gaussian=cv2.GaussianBlur(image,(7,7),0)<br>
cv2.imshow('Gaussian Blurring',Gaussian)<br>
cv2.waitKey(0)<br>

#median blur<br>
median=cv2.medianBlur(image,10)<br>
cv2.imshow('Median Blurring',median)<br>
cv2.waitKey(0)<br>

#bilateral blur<br>
bilateral=cv2.bilateralFilter(image,9,75,75)<br>
cv2.imshow('bilateral Blurring',bilateral)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>

**OUTPUT**<br>

![image](https://user-images.githubusercontent.com/97940767/176425171-1196156a-09e6-4db8-a01d-aa5ee13a58a4.png)<br>
![image](https://user-images.githubusercontent.com/97940767/176425214-38d5224a-b05d-429e-892e-4178fef35439.png)<br>
![image](https://user-images.githubusercontent.com/97940767/176425274-6d5cca91-fbd3-4045-9864-e0bbb159be21.png)<br>
![image](https://user-images.githubusercontent.com/97940767/176425325-ea476067-cfe1-4bc6-a992-13c5e65feb71.png)<br>


**17.develop image using enhacement**

from PIL import Image<br>
from PIL import ImageEnhance<br>
image=Image.open('a2.jpg')<br>
image.show()<br>
<br>
enh_bri=ImageEnhance.Brightness(image)<br>
brightness=1.5<br>
image_brightened=enh_bri.enhance(brightness)<br>
image_brightened.show()<br>

enh_col=ImageEnhance.Color(image)<br>
color=1.5<br>
image_colored=enh_col.enhance(color)<br>
image_colored.show()<br>

enh_con=ImageEnhance.Contrast(image)<br>
contrast=1.5<br>
image_contrasted=enh_con.enhance(contrast)<br>
image_contrasted.show()<br>

enh_sha=ImageEnhance.Sharpness(image)<br>
sharpness=1.5<br>
image_Sharped=enh_con.enhance(sharpness)<br>
image_Sharped.show()<br>

**OUTPUT**<br>

![image](https://user-images.githubusercontent.com/97940767/176423684-f670bc1b-d791-40a7-9702-9791b86fc177.png)<br>
![image](https://user-images.githubusercontent.com/97940767/176423944-d8e1cc4c-74f1-4bde-b321-4f18cdfdb94e.png)<br>
![image](https://user-images.githubusercontent.com/97940767/176424023-7f2d6c78-c3f9-4efe-9799-fb5ce37b23e2.png)<br>
![image](https://user-images.githubusercontent.com/97940767/176424059-62f1282b-a76e-4293-8261-5a69d4ac5be8.png)<br>
![image](https://user-images.githubusercontent.com/97940767/176424101-149ea877-13c1-4728-b9c8-f52d55c9e9f5.png)<br>
<br>

18)MORPHOLOGICAL OPERATIONS<br>

import cv2<br>
import numpy as np
from matplotlib import pyplot as plt<br>
from PIL import Image,ImageEnhance<br>
img=cv2.imread('b2.jpg',0)<br>
ax=plt.subplots(figsize=(20,10))<br>
kernel=np.ones((5,5),np.uint8)<br>
opening=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)<br>
closing=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)<br>
erosion=cv2.erode(img,kernel,iterations=1)<br>
dilation=cv2.dilate(img,kernel,iterations=1)<br>
gradient=cv2.morphologyEx(img,cv2.MORPH_GRADIENT,kernel)<br>
plt.subplot(151)<br>
plt.imshow(opening)<br>
plt.subplot(152)<br>
plt.imshow(closing)<br>
plt.subplot(153)<br>
plt.imshow(erosion)<br>
plt.subplot(154)<br>
plt.imshow(dilation)<br>
plt.subplot(155)<br>
plt.imshow(gradient)<br>
cv2.waitKey(0)<br>

**OUTPUT**<br>

![image](https://user-images.githubusercontent.com/97940767/176427092-f4b3d9f4-065c-4f5b-911c-f72c78b062da.png)<br>

**19) develop a program to !) read an image
                         !!)write (save) the grayscale image
                         !!!) Display the original image and grayscale image**
                         
import cv2<br>
OriginalImag=cv2.imread('r1.jpg')<br>
GrayImg=cv2.imread('r1.jpg',0)<br>
isSaved=cv2.imwrite('D:\ashmitha\r1.jpg',GrayImg)<br>
cv2.imshow('Display original Image',OriginalImag)<br>
cv2.imshow('Display Grayscale Image',GrayImg)<br>
cv2.waitKey(0)<br>
cv2.distroyAllWindows()<br>
if isSaved:<br>
    print('the image is successfully saved')   <br>                   

**OUTPUT**<br>

![image](https://user-images.githubusercontent.com/97940767/178700926-c1c0d145-3d19-4bbc-8802-b7efe0c23811.png)<br> 
![image](https://user-images.githubusercontent.com/97940767/178700983-2981daa7-2d44-4c3c-a30f-e5c5300edc2f.png)<br> 
![image](https://user-images.githubusercontent.com/97940767/178705689-7bb3f0cc-79f2-4453-b9ea-fa8e8540ae13.png)<br> 
![image](https://user-images.githubusercontent.com/97940767/178719201-1f3f0e33-856f-4abf-8953-9cc4de2b77ba.png)



**20) slicing with background.jpg**<br>

import cv2<br>
import numpy as np<br>
from matplotlib import pyplot as plt<br>
image=cv2.imread('r1.jpg',0)<br>
x,y=image.shape<br>
z=np.zeros((x,y))<br>
for i in range(0,x):<br>
    for j in range(0,y):<br>
        if (image[i][j]>50and image[i][j]<150):<br>
            z[i][j]=255<br>
        else: <br>
            z[i][j]=image[i][j]<br>
equ=np.hstack((image,z)) <br> <br>   
plt.title('gray level slicing with background')<br>
plt.imshow(equ,'gray')<br>
plt.show()<br>
            
**OUTPUT**<br>


![image](https://user-images.githubusercontent.com/97940767/178707065-bba54fc6-02ea-4e86-bf0e-1c25ac1fe53b.png)<br>

21) slicing without background.jpg**<br>

import cv2
import numpy as np<br>
from matplotlib import pyplot as plt<br>
image=cv2.imread('r1.jpg',0)<br>
x,y=image.shape<br>
z=np.zeros((x,y))<br>
for i in range(0,x):<br>
    for j in range(0,y):<br>
        if (image[i][j]>50and image[i][j]<150):<br>
            z[i][j]=255<br>
        else: 
            z[i][j]=0<br>
equ=np.hstack((image,z)) <br>     
plt.title('gray level slicing without background')<br>
plt.imshow(equ,'gray')<br>
plt.show()<br>

**OUTPUT**<br>

![image](https://user-images.githubusercontent.com/97940767/178708416-2124ab67-4013-4510-8b1a-72283ea898fb.png)<br>

22) ANALYSE THE IMAGE DATA USING HISTOGRAM

import numpy as np<br>
import cv2 as cv<br>
from matplotlib import pyplot as plt<br>
img = cv.imread('r1.jpg')<br>
plt.imshow(img)<br>
plt.show()<br>
img = cv.imread('r1.jpg',0)<br>
plt.hist(img.ravel(),256,[0,256]);<br>
plt.show()<br> 

**OUTPUT**<br>

![image](https://user-images.githubusercontent.com/97940767/178960607-d9ad5d84-396b-4161-b6e4-fb471db5499d.png)

from skimage import io<br> 
import matplotlib.pyplot as plt<br> 
img = io.imread('r1.jpg')<br> 
plt.imshow(img)<br> 
plt.show()<br> 
image = io.imread('r1.jpg')<br> 
ax = plt.hist(image.ravel(), bins = 256)<br> 
plt.show()<br> 

**OUTPUT**<br>

![image](https://user-images.githubusercontent.com/97940767/178960943-c23111ab-1eaf-4184-984d-eabf9e7f335e.png)

from skimage import io<br>
import matplotlib.pyplot as plt<br>
image = io.imread('r1.jpg')<br>

_ = plt.hist(image.ravel(), bins = 256, color = 'orange', )<br>
_ = plt.hist(image[:, :, 0].ravel(), bins = 256, color = 'red', alpha = 0.5)<br>
_ = plt.hist(image[:, :, 1].ravel(), bins = 256, color = 'Green', alpha = 0.5)<br>
_ = plt.hist(image[:, :, 2].ravel(), bins = 256, color = 'Blue', alpha = 0.5)<br>
_ = plt.xlabel('Intensity Value')<br>
_ = plt.ylabel('Count')<br>
_ = plt.legend(['Total', 'Red_Channel', 'Green_Channel', 'Blue_Channel'])<br>
plt.show()<br>

**OUTPUT**<br>

![image](https://user-images.githubusercontent.com/97940767/178961163-c842fd70-c768-400d-8641-e3316aa990e9.png)

