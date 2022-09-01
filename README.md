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

#22) ANALYSE THE IMAGE DATA USING HISTOGRAM

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

![image](https://user-images.githubusercontent.com/97940767/178961163-c842fd70-c768-400d-8641-e3316aa990e9.png)<br><br>

from matplotlib import pyplot as plt<br>
import numpy as np<br>
fig,ax = plt.subplots(1,1)<br>
a = np.array([22,87,5,43,56,73,55,54,11,20,51,5,79,31,27])<br>
ax.hist(a, bins = [0,25,50,75,100])<br>
ax.set_title("histogram of result")<br>
ax.set_xticks([0,25,50,75,100])<br>
ax.set_xlabel('marks')<br>
ax.set_ylabel('no. of students')<br>
plt.show()<br>

**OUTPUT**<br>

![image](https://user-images.githubusercontent.com/97940767/178961828-fa93db8f-63ff-4f2d-9e59-4c9e98df6bd0.png)<br>

23) Program to perform basic image data analysis using intensity transformation<br>
 a)image negative<br>
 b)log transformation<br>
 c)gamma correction<br>
 
 %matplotlib inline<br>
import imageio<br>
import matplotlib.pyplot as plt<br>
import warnings<br>
import matplotlib.cbook<br>
warnings.filterwarnings("ignore",category=matplotlib.cbook.mplDeprecation)<br>
pic=imageio.imread('r1.jpg')<br>
plt.figure(figsize=(6,6))<br>
plt.imshow(pic);<br>
plt.axis('off');<br>

![image](https://user-images.githubusercontent.com/97940767/179962602-b4666fc8-5475-4734-b079-af27d9f77f78.png)<br>


negative=255-pic<br>
plt.figure(figsize=(6,6))<br>
plt.imshow(negative);<br>
plt.axis('off');<br>
<br>
![image](https://user-images.githubusercontent.com/97940767/179962726-672f57ac-52f7-4e59-a516-eee025150d8d.png)<br>

%matplotlib inline<br>
import imageio<br>
import numpy as np<br>
import matplotlib.pyplot as plt<br>
pic=imageio.imread('r1.jpg')<br>
gray=lambda rgb:np.dot(rgb[...,:3],[0.299,0.587,0.114])<br>
gray=gray(pic)<br>

max_=np.max(gray)<br>

def log_transform():<br>
    return(255/np.log(1+max_))*np.log(1+gray)<br>
plt.figure(figsize=(5,5))<br>
plt.imshow(log_transform(),cmap=plt.get_cmap(name='gray'))<br>
plt.axis('off');<br>

![image](https://user-images.githubusercontent.com/97940767/179962999-f631a48a-c142-4c44-9ac3-ea83756d4ea7.png)<br>


import imageio<br>
import matplotlib.pyplot as plt<br>
pic=imageio.imread('r1.jpg')<br>
gamma=2.2<br>
gamma_correction=((pic/255)**(1/gamma))<br>
plt.figure(figsize=(5,5))<br>
plt.imshow(gamma_correction)<br>
plt.axis('off');<br>

![image](https://user-images.githubusercontent.com/97940767/179963155-07040a76-7b55-40b3-a1c1-c8d7d1dc8005.png)<br>


24) Program to perform basic Image manipulations
     a)sharpness<br>
     b)flipping<br>
     c)cropping<br>
 
 from PIL import Image<br>
from PIL import ImageFilter<br>
import matplotlib.pyplot as plt<br>
 
my_image=Image.open('r2.jpg')<br>

sharp=my_image.filter(ImageFilter.SHARPEN)<br>

sharp.save('D:/image_sharpen.jpg')<br>
sharp.show()<br>
plt.imshow(sharp)<br>
plt.show()<br>

![image](https://user-images.githubusercontent.com/97940767/179965718-975e4c05-cb78-45b3-a895-b0643890693d.png)<br>

import matplotlib.pyplot as plt<br>
image=Image.open('r2.jpg')<br>
plt.imshow(image)<br>
plt.show()<br>

flip=image.transpose(Image.FLIP_LEFT_RIGHT)<br>

flip.save('D:/image_flip.jpg')<br>
plt.imshow(flip)<br>
plt.show()<br>

![image](https://user-images.githubusercontent.com/97940767/179965981-f47de189-0e42-4d76-ab14-ffe8e0687100.png)<br>


from PIL import Image<br>
import matplotlib.pyplot as plt<br>
im=Image.open('r2.jpg')<br>
plt.imshow(im)<br>
plt.show()<br>
width,height=im.size<br>
im1=im.crop((50,25,200,150))<br>

#im1.show()<br>
plt.imshow(im1)<br>
plt.show()<br>

![image](https://user-images.githubusercontent.com/97940767/179966391-ce4ad578-76e2-45c7-81f9-39728781df1b.png)<br>



from PIL import Image<br>
import numpy as np<br>
w, h = 600, 600<br>
data = np.zeros((h, w, 3), dtype=np.uint8)<br>
data[0:100, 0:100] = [255, 0, 0]<br>
data[100:200, 100:200] = [255, 0, 255]<br>
data[200:300, 200:300] = [0, 255, 0]<br>
data[300:400, 300:400] = [130, 255, 0]<br>
data[400:500, 400:500] = [0, 255, 170]<br>
data[500:600, 500:600] = [180, 255, 0]<br>
#red patch in upper left<br>
img = Image.fromarray(data, 'RGB')<br>
img.save('my.png')<br>
plt.imshow(img)<br>
plt.show()<br>

OUTPUT<br>

![image](https://user-images.githubusercontent.com/97940767/180202141-ddc10a60-8b2e-4025-b917-73329b649a86.png)<br>

import numpy as np<br>
import matplotlib.pyplot as plt<br>

arr = np.zeros((256,256,3), dtype=np.uint8)<br>
imgsize = arr.shape[:2]<br>
innerColor = (255, 255, 255)<br>
outerColor = (0, 0, 0)<br>
for y in range(imgsize[1]):<br>
    for x in range(imgsize[0]):<br>
        #Find the distance to the center<br>
        distanceToCenter = np.sqrt((x - imgsize[0]//2) ** 2 + (y - imgsize[1]//2) ** 2)<br>

        #Make it on a scale from 0 to 1innerColor<br>
        distanceToCenter = distanceToCenter / (np.sqrt(2) * imgsize[0]/2)<br>

        #Calculate r, g, and b values<br>
        r = outerColor[0] * distanceToCenter + innerColor[0] * (1 - distanceToCenter)<br>
        g = outerColor[1] * distanceToCenter + innerColor[1] * (1 - distanceToCenter)<br>
        b = outerColor[2] * distanceToCenter + innerColor[2] * (1 - distanceToCenter)<br>
        # print r, g, b<br>
        arr[y, x] = (int(r), int(g), int(b))<br>

plt.imshow(arr, cmap='gray')<br>
plt.show()<br>


OUTPUT<br>

![image](https://user-images.githubusercontent.com/97940767/180202631-3e092d68-f590-4a94-b16c-68a3ab0c76f4.png)<br>


1)maximum


import cv2<br>
import numpy as np<br>
import matplotlib.pyplot as plt<br>
img=cv2.imread('r1.jpg' )<br>
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)<br>
plt.imshow(img)<br>
plt.show()<br>
max_channels = np.amax([np.amax(img[:,:,0]), np.amax(img[:,:,1]),np.amax(img[:,:,2])])<br>

print(max_channels)<br>

output<br>

![image](https://user-images.githubusercontent.com/97940767/181231478-d351b176-cb25-4cb3-b052-5fc9828a0e48.png)<br>

<br>
MINIMUM

import imageio<br>
import numpy as np<br>
import matplotlib.pyplot as plt<br>
img=imageio.imread('r1.jpg' )<br>
plt.imshow(img)<br>
plt.show()<br>
min_channels = np.amin([np.min(img[:,:,0]), np.amin(img[:,:,1]),np.amin(img[:,:,2])])<br>

print(min_channels)<br>

OUTPUT<br>

![image](https://user-images.githubusercontent.com/97940767/181231660-a69f6a51-6908-40f5-8651-a42868888ce6.png)<br>


AVERAGE<br>

import cv2<br>
import matplotlib.pyplot as plt<br>
import numpy as np<br>
img=cv2.imread('r1.jpg')<br>
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)<br>
plt.imshow(img)<br>
np.average(img)<br>

OUTPUT<br>
![image](https://user-images.githubusercontent.com/97940767/181231889-c4c7c404-9673-4271-84c4-8256928a51f1.png)

STANDARD DEVIATION<br>

from PIL import Image,ImageStat<br>
import matplotlib.pyplot as plt<br>
im=Image.open('r1.jpg')<br>
plt.imshow(im)<br>
plt.show()<br>
stat=ImageStat.Stat(im)<br>
print(stat.stddev)<br>

OUTPUT

![image](https://user-images.githubusercontent.com/97940767/181232364-41def64b-1342-4a4e-83c9-ab5ff7142eb9.png)



#  Python3 program for printing<br>
# the rectangular pattern<br>
 <br>
# Function to print the pattern<br>
def printPattern(n):<br>
 
    arraySize = n * 2 - 1;<br>
    result = [[0 for x in range(arraySize)]<br>
                 for y in range(arraySize)];<br>
         
    # Fill the values<br>
    for i in range(arraySize):<br>
        for j in range(arraySize):<br>
            if(abs(i - (arraySize // 2)) ><br>
               abs(j - (arraySize // 2))):<br>
                result[i][j] = abs(i - (arraySize // 2));<br>
            else:<br>
                result[i][j] = abs(j - (arraySize // 2));<br>
             
    # Print the array<br>
    for i in range(arraySize):<br>
        for j in range(arraySize):<br>
            print(result[i][j], end = " ");<br>
        print("");
 
# Driver Code<br><br>
n = 4;<br><br>
 
printPattern(n);<br><br>


OUTPUT<br>

![image](https://user-images.githubusercontent.com/97940767/181450782-bf66735d-3647-4541-96bd-c961391e62d7.png)<br>


import numpy as np<br>
from PIL import Image<br>
import matplotlib.pyplot as plt<br>
def printPattern(n):<br>

    arraySize = n * 2 - 1;<br>
    result = [[0 for x in range(arraySize)]<br>
                 for y in range(arraySize)];<br>
         
    # Fill the values<br>
    for i in range(arraySize):<br>
        for j in range(arraySize):<br>
            if(abs(i - (arraySize // 2)) ><br>
               abs(j - (arraySize // 2))):<br>
                result[i][j] = abs(i - (arraySize // 2));<br>
            else:<br>
                result[i][j] = abs(j - (arraySize // 2));<br>
             
    # Print the array<br>
    for i in range(arraySize):<br>
        for j in range(arraySize):<br>
            print(result[i][j], end = " ");<br>
        print("");<br>
 
# Driver Code<br>
n = 3;<br>
 
printPattern(n);<br>
w, h = n,n<br>
arraySize = np.zeros((h, w, 3))# dtype=np.uint8)<br>
arraySize[0:n, 0:n] = [255,0,0] # red patch in upper left<br>
#arraySize[0:n, 0:n] = [255, 0, 0]<br>
#arraySize[n:0,n:0] = [120,200,255]<br>
img = Image.fromarray(arraySize, 'RGB')<br>
plt.imshow(img)<br>
plt.show()<br>
#img.save('my.png')<br>
#img.show()<br>


OUTPUT<br>

![image](https://user-images.githubusercontent.com/97940767/181451145-50d3f376-baac-48d4-8e39-017a438fd9a2.png)<br>

import matplotlib.pyplot as plt<br>
       
M =    ([2, 2, 2, 2, 2],<br>  
        [2, 1, 1, 1, 2],<br>  
        [2, 1, 0, 1, 2],<br>  
        [2, 1, 1, 1, 2],<br>
        [2, 2, 2, 2, 2])<br>  
plt.imshow(M,cmap='Blues')<br>
plt.show()<br>

OUTPUT<br>

![image](https://user-images.githubusercontent.com/97940767/181451374-96755805-6f22-4b52-828a-d2147aaca693.png)<br>

#MINIMUM

import imageio<br>
import numpy as np<br>
import matplotlib.pyplot as plt<br>
img=imageio.imread('r1.jpg' )<br>
plt.imshow(img)<br>
plt.show()<br>
min_channels = np.amin([np.min(img[:,:,0]), np.amin(img[:,:,1]),np.amin(img[:,:,2])])<br>

print(min_channels)<br>

OUTPUT

![image](https://user-images.githubusercontent.com/97940767/186384659-53a78406-e0ac-44a8-bbb5-6774f40a39ce.png)<br>


#MAXIMUM

import cv2<br>
import numpy as np<br>
import matplotlib.pyplot as plt<br>
img=cv2.imread('r1.jpg' )<br>
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)<br>
plt.imshow(img)<br>
plt.show()<br>
max_channels = np.amax([np.amax(img[:,:,0]), np.amax(img[:,:,1]),np.amax(img[:,:,2])])<br>

print(max_channels)<br>

OUTPUT

![image](https://user-images.githubusercontent.com/97940767/186385225-9fd66a0e-0647-4603-a15b-84bf4c5f101e.png)


#MEAN MEDIUM STANDARD DEVIATION

from PIL import Image,ImageStat<br>
import matplotlib.pyplot as plt<br>
im=Image.open('r1.jpg')<br>
plt.imshow(im)<br>
plt.show()<br>
stat=ImageStat.Stat(im)<br>
print(stat.stddev)<br>

OUTPUT

![image](https://user-images.githubusercontent.com/97940767/186385868-bab00c60-c8bc-4fa5-a1ac-f2f06d58afd6.png)


#AVERAGE

import cv2<br>
import matplotlib.pyplot as plt<br>
import numpy as np<br>
img=cv2.imread('r1.jpg')<br>
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)<br>
plt.imshow(img)<br>
np.average(img)<br>

OUTPUT<br>

![image](https://user-images.githubusercontent.com/97940767/186386370-16faac91-d10a-4d8c-b4b2-8d0bef78c25e.png)<br>


import cv2<br>
# Read the original image<br>
img = cv2.imread('a1.jpg')<br>
# Display original image<br>
cv2.imshow('Original', img)<br>
cv2.waitKey(0)<br>
# Convert to graycsale<br>
img_gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)<br>
# Blur the image for better edge detection<br>
img_blur = cv2.GaussianBlur(img_gray, (3,3), 0)<br>
# Sobel Edge Detection<br>
sobelx = cv2.Sobel(src=img_blur, ddepth=cv2.CV_64F, dx=1, dy=0, ksize=5) # Sobel Edge Detection on the X axis<br>
sobely = cv2.Sobel(src=img_blur, ddepth=cv2.CV_64F, dx=0, dy=1, ksize=5) # Sobel Edge Detection on the Y axis<br>
sobelxy = cv2.Sobel(src=img_blur, ddepth=cv2.CV_64F, dx=1, dy=1, ksize=5) # Combined X and Y Sobel Edge Detection<br>
# Display Sobel Edge Detection Images<br>
cv2.imshow('Sobel X', sobelx)<br>
cv2.waitKey(0)<br>
cv2.imshow('Sobel Y', sobely)<br>
cv2.waitKey(0)<br>
cv2.imshow('Sobel X Y using Sobel() function', sobelxy)<br>
cv2.waitKey(0)<br>
# Canny Edge Detection<br>
edges = cv2.Canny(image=img_blur, threshold1=100, threshold2=200) # Canny Edge Detection<br>
# Display Canny Edge Detection Image<br>
cv2.imshow('Canny Edge Detection', edges)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>

OUTPUT<br>

![image](https://user-images.githubusercontent.com/97940767/186404662-e61a42d9-73e7-4233-bf9f-b22c63b23f48.png)<br>
![image](https://user-images.githubusercontent.com/97940767/186404698-c8bd89d9-a8b7-402b-ba42-2ae04caa6e1c.png)<br>
![image](https://user-images.githubusercontent.com/97940767/186404742-7446316c-f00a-4f73-aa13-136a65bf5fab.png)<br>
![image](https://user-images.githubusercontent.com/97940767/186404788-662a32ef-c5a2-4dfe-a317-d5bdf7c38bc0.png)<br>
![image](https://user-images.githubusercontent.com/97940767/186404834-79316f1a-cf74-48b4-b5e9-d894eb457b25.png)<br>


USING PILLOW FUNCTIONS

from PIL import Image, ImageChops, ImageFilter <br>
from matplotlib import pyplot as plt<br>
#Create a PIL Image objects<br>
x = Image.open("a1.png")<br>
o =Image.open("a2.png")<br>
#Find out attributes of Image Objects <br>
print('size of the image: ', x.size,' colour mode:', x.mode)<br>
print('size of the image: ', o.size,' colour mode:', o.mode)<br>
#plot 2 images one besides the other<br>
plt.subplot(121), plt.imshow(x) <br>
plt.axis('off')<br>
plt.subplot(122), plt.imshow(o)<br>
plt.axis('off')<br>
#multiply images<br>
merged = ImageChops.multiply(x,o)<br>
#adding 2 images <br>
add = ImageChops.add(x,o)<br>
#convert colour mode<br><br>
greyscale = merged.convert('L')<br>
greyscale<br>


OUTPUT<br>

![image](https://user-images.githubusercontent.com/97940767/186653308-1b0d3920-98e4-480e-8d3d-c6a32fd7f157.png)<br>


#More Attributes<br>
image=merged<br>

print(' image size: ',image.size,<br>
     '\ncolor mode: ',image.mode,<br>
     '\ncolor width: ',image.width, '|also represented by:',image.size[0],<br>
     '\ncolor height: ',image.height, '|also represented by:',image.size[1], )<br>
     
     #OUTPUT<br>
     
![image](https://user-images.githubusercontent.com/97940767/186653508-4433d25e-0743-4bd4-97c1-82d05ff8f542.png)

#mapping the pixels of the image so we can use them as coordinates 
pixel = greyscale.load()
#a nested Loop to parse through all the pixels in the image
for row in range (greyscale.size[0]):
 for column in range(greyscale.size[1]): 
    if pixel[row, column] != (255):
     pixel [row, column] = (0)
greyscale
     
     
#OUTPUT<br>

![image](https://user-images.githubusercontent.com/97940767/186653719-7957c799-1d68-4e70-83b4-344a06efa89c.png)<br>



#1. invert image<br>
invert = ImageChops.invert(greyscale) <br>

#2. invert by subtraction<br>

bg = Image.new('L', (256, 256), color=(255)) #create a new image with a solid white background <br>
subt = ImageChops.subtract(bg, greyscale) #subtract image from background<br>

#3. rotate<br>
rotate = subt.rotate(45) <br>
rotate<br>

#OUTPUT<br>

![image](https://user-images.githubusercontent.com/97940767/186653897-0632adae-b9fc-4c07-978e-f7a199bc07b7.png)<br>


#gaussian blur<br>
blur = greyscale.filter(ImageFilter.GaussianBlur (radius=1))<br>

#edge detection<br>
edge = blur.filter(ImageFilter.FIND_EDGES)<br>
edge<br>

#OUTPUT<br>

![image](https://user-images.githubusercontent.com/97940767/186654163-5c039603-1fc2-4d2d-b19b-faf266b82da6.png)<br>


#change edge colours<br>
edge = edge.convert('RGB')<br>
bg_red = Image.new('RGB', (256,256), color=(255,0,0))<br>

filled_edge = ImageChops.darker (bg_red, edge)<br>
filled_edge<br>

![image](https://user-images.githubusercontent.com/97940767/186654383-6abd271e-24b7-43f6-a23b-9dac3de8273c.png)<br>

#save image in the directory<br>
edge.save('processed.png')<br>




image restoration<br>


import numpy as np<br>
import cv2<br>
import matplotlib.pyplot as plt<br>
#Open the image.<br>
img= cv2.imread('dimage_damaged.png')<br>
plt.imshow(img)<br>
plt.show()<br>
#Load the mask.<br>
mask= cv2.imread('dimage_mask.png', 0)<br>
plt.imshow(mask)<br>
plt.show()<br>
# Inpaint.<br>
dst = cv2.inpaint (img, mask, 3, cv2.INPAINT_TELEA)<br>
# write the output.<br>
cv2.imwrite('dimaged_inpainted.png', dst)<br>
plt.imshow(dst)<br>
plt.show()<br>


OUTPUT<br>

![image](https://user-images.githubusercontent.com/97940767/187874939-2efaf180-f505-40a4-bae3-d4f8b9ca3d88.png)<br>
![image](https://user-images.githubusercontent.com/97940767/187875009-8b5d632d-2814-4b54-a5b8-fdc2ea237599.png)<br>


import numpy as np<br>
import matplotlib.pyplot as plt<br>
import pandas as pd<br>
plt.rcParams['figure.figsize'] = (10, 8)<br>



def show_image(image, title='Image', cmap_type='gray'):<br>
    plt.imshow(image, cmap=cmap_type)<br>
    plt.title(title)<br>
    plt.axis('off') <br>
    
def plot_comparison (img_original, img_filtered, img_title_filtered):<br>
    fig, (ax1, ax2) = plt.subplots(ncols=2, figsize=(10, 8), sharex=True, sharey=True)<br>
    ax1.imshow(img_original, cmap=plt.cm.gray)<br>
    ax1.set_title('Original')<br>
    ax1.axis('off')<br>
    ax2.imshow(img_filtered, cmap=plt.cm.gray)<br>
    ax2.set_title(img_title_filtered)<br>
    ax2.axis('off')<br>
    
    
    from skimage.restoration import inpaint<br>
from skimage.transform import resize<br>
from skimage import color<br>




image_with_logo = plt.imread('imlogo.png')<br>

#Initialize the mask<br>
mask = np.zeros(image_with_logo.shape[:-1])<br>

# Set the pixels where the Logo is to 1 <br>
mask[210:272, 360:425] = 1<br>
<br>
# Apply inpainting to remove the Logo<br>
image_logo_removed = inpaint.inpaint_biharmonic(image_with_logo,<br>
                                             mask,<br>
                                             multichannel=True)<br>

#Show the original and Logo removed images<br>
plot_comparison (image_with_logo, image_logo_removed, 'Image with logo removed')<br>


OUTPUT<br><br>

![image](https://user-images.githubusercontent.com/97940767/187875861-1f0db53c-f00e-4a73-8a88-ac8c4fecc720.png)<br>



from skimage.util import random_noise<br>

fruit_image= plt.imread('fruitts.jpeg')<br><br>

#Add noise to the image<br>
noisy_image = random_noise (fruit_image)<br>

#Show th original and resulting image <br>
plot_comparison (fruit_image, noisy_image, 'Noisy image')<br>

OUTPUT<br>

![image](https://user-images.githubusercontent.com/97940767/187876704-a0d76608-1eef-405d-bbc3-7200830caf0c.png)<br>


from skimage.restoration import denoise_tv_chambolle<br>

noisy_image = plt.imread('noisy.jpg')<br>

# Apply total variation filter denoising <br>
denoised_image = denoise_tv_chambolle (noisy_image, multichannel=True)<br>

#Show the noisy and denoised image<br>
plot_comparison (noisy_image, denoised_image, 'Denoised Image')<br>


![image](https://user-images.githubusercontent.com/97940767/187878141-f1d7343c-ed8f-45ce-8e2d-994139bfb233.png)<br>



from skimage.restoration import denoise_bilateral<br>
landscape_image = plt.imread('noisy.jpg')<br>
#Apply bilateral filter denoising<br>
denoised_image = denoise_bilateral (landscape_image, multichannel=True)<br>
#Show original and resulting images<br>
plot_comparison (landscape_image, denoised_image, 'Denoised Image')<br>


OUTPUT<br>

![image](https://user-images.githubusercontent.com/97940767/187878683-a77a6822-92ae-4cca-a229-cc9f39ae13fb.png)<br>


def show_image_contour (image, contours): <br>
    plt.figure()<br>
    for n, contour in enumerate(contours):<br>
        plt.plot(contour[:, 1], contour[:, 0], linewidth=3)<br>
    plt.imshow(image, interpolation='nearest', cmap='gray_r')<br>
    plt.title('Contours')<br>
    plt.axis('off')<br>
    
    <br>
    from skimage import measure, data<br>

#Obtain the horse image<br>
horse_image = data.horse()<br>

#Find the contours with a constant Level value of 0.8 <br>
contours = measure.find_contours (horse_image, level=0.8)<br>

#Shows the image with contours found <br>
show_image_contour (horse_image, contours)<br>

![image](https://user-images.githubusercontent.com/97940767/187878928-44bb84cf-451d-4d65-b49a-3911b11c8016.png)<br>


from skimage.io import imread <br>
from skimage.filters import threshold_otsu<br>

image_dices = imread('diceimg.png')<br>

# Make the image grayscale<br>
image_dices = color.rgb2gray(image_dices)<br>

#Obtain the optimal thresh value <br>
thresh = threshold_otsu(image_dices)<br>

# Apply thresholding<br>
binary=image_dices > thresh<br>

# Find contours at a constant value of 0.8<br>
contours = measure.find_contours (binary, level=0.8)<br>

# Show the image<br>
show_image_contour (image_dices, contours)<br>

![image](https://user-images.githubusercontent.com/97940767/187879003-4a6ab850-9330-44c4-ae34-ebbf9489b2b7.png)<br>


# Create List with the shape of each contour <br>
shape_contours = [cnt.shape[0] for cnt in contours]<br>

#Set 50 as the maximum size of the dots shape <br>
max_dots_shape = 50<br><br>

#Count dots in contours excluding bigger than dots size <br>
dots_contours = [cnt for cnt in contours if np.shape(cnt) [0] < max_dots_shape]<br>

#Shows all contours found <br>
show_image_contour (binary, contours)<br>

#Print the dice's number<br>
print('Dices dots number: {}.'.format(len (dots_contours)))<br>


![image](https://user-images.githubusercontent.com/97940767/187879190-7ca8e097-5b2d-440e-b7f4-4ac6baeb54b4.png)<br>


