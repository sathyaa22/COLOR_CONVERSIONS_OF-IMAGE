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

## Program:
### Developed By: J.JENISHA
### Register Number: 212222230056
<table>
  <tr>
    <td width=50%>

### i) Read and display the image
```Python
    import cv2
img=cv2.imread('anime.jpg',1)
img=cv2.resize(img,(400,300))
cv2.imshow('show',img)
cv2.waitKey(0)
cv2.destroyAllWindows()

``` 
  </td>
  <td>

### OUTPUT:

 <img src="https://github.com/Jenishajustin/COLOR_CONVERSIONS_OF-IMAGE/assets/119405070/082fee7a-809f-45bd-9a61-0acaf4cbf827">
  </td>
  </tr>

   <tr>
    <td width=50%>

### ii)Write the image
```Python
    import cv2
img=cv2.imread('anime.jpg')
re=cv2.resize(img,(400,300))
cv2.imwrite('display.jpg',re)
cv2.imshow('display',re)

```
  </td>
  <td>

### OUTPUT:

<img src="https://github.com/Jenishajustin/COLOR_CONVERSIONS_OF-IMAGE/assets/119405070/df6997f8-d5dd-4a18-9e41-02a995bb0b13">
  </td>
  </tr>
  <tr>
    <td width=50%>

### iii)Shape of the Image
```Python
import cv2
image=cv2.imread('anime.jpg')
print(image.shape)

```
  </td>
  <td>

### OUTPUT:
<img src="https://github.com/Jenishajustin/COLOR_CONVERSIONS_OF-IMAGE/assets/119405070/f9903b8c-bd1c-47de-bae4-e705369ab3cf">
  </td>
  </tr>
  <tr>
    <td>
      
### iv)Access rows and columns
```Python
    import random
import cv2
img=cv2.imread('anime.jpg',1)
re=cv2.resize(img,(300,300))
for i in range (150,200):
    for j in range(re.shape[1]):
        re[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
cv2.imshow('part image',re)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
  </td>
  <td width="50%">

### OUTPUT:

 <img src="https://github.com/Jenishajustin/COLOR_CONVERSIONS_OF-IMAGE/assets/119405070/25b96b9d-6d6c-48cc-aab4-2e7532fc1c14">
  </td>
  </tr>
  <tr>
    <td width=50%>
      
### v)Cut and paste portion of image

 ```Python
    import cv2
img=cv2.imread('anime.jpg',1)
re=cv2.resize(img,(400,400))
tag =re[150:200,110:160]
re[110:160,150:200] = tag
cv2.imshow('cut image',re)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
  </td>
  <td>
    
### OUTPUT:

<img src="https://github.com/Jenishajustin/COLOR_CONVERSIONS_OF-IMAGE/assets/119405070/5ebf3e0a-6992-46a0-bc13-c5ed27105adc">
  </td>
  </tr>
</table>

### vi) BGR and RGB to HSV and GRAY
```Python
import cv2
img = cv2.imread('niru.jpg',1)
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

### OUTPUT:

![WhatsApp Image 2024-02-12 at 22 21 57_a92d98dc](https://github.com/niraunjana/COLOR_CONVERSIONS_OF-IMAGE/assets/119395610/19799dd5-cab6-4344-bd5b-e9301f80a6b7)


### vii) HSV to RGB and BGR
```Python
import cv2
img = cv2.imread('niru.jpg')
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

### OUTPUT:

![WhatsApp Image 2024-02-12 at 22 22 46_9835eea4](https://github.com/niraunjana/COLOR_CONVERSIONS_OF-IMAGE/assets/119395610/550aedc3-8dac-4542-8f59-8cc4175b91ef)


### viii) RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('niru.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```



## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







