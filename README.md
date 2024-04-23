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

### Developed By: SRI SAI PRIYA.S
### Register Number: 212222240103

##### Program:
### i) Read and display the image
```
import cv2
image = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\nat.jpg')
resized_image = cv2.resize(image, (200, 300))
cv2.imshow('Sri Sai priya', resized_image)    
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![WhatsApp Image 2024-02-19 at 08 03 11_5556a4de](https://github.com/SriSaiPriyaSenthilvel/COLOR_CONVERSIONS_OF-IMAGE/assets/119475702/8b158c55-db0c-4f11-85f7-96c14130db96)

### ii)Write the image:

##### Program:
```
import cv2
image=cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\nat.jpg')
cv2.imwrite('demos.jpg',image)
```
<br>
<br>
<br>
<br>
<br>
<br>

## Output:

![image](https://github.com/SriSaiPriyaSenthilvel/COLOR_CONVERSIONS_OF-IMAGE/assets/119475702/ab71d3ca-94ea-4473-ab91-e876ae1f0db4)

<br>
<br>

### iii)Shape of the Image:

##### Program:
```
import cv2
image=cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\nat.jpg')
print(image.shape)
```
## Output:

![image](https://github.com/SriSaiPriyaSenthilvel/COLOR_CONVERSIONS_OF-IMAGE/assets/119475702/a46a004b-3dac-486a-8a4b-cbda42daeeb8)

<br>
<br>

### iv)Access rows and columns:

##### Program:
```
    import random
    import cv2
    image=cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\nat.jpg')
    image=cv2.resize(image,(500,500))
    for i in range (250,500):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```

<br>
<br>
<br>
<br>
<br>
<br>

## Output:

![image](https://github.com/SriSaiPriyaSenthilvel/COLOR_CONVERSIONS_OF-IMAGE/assets/119475702/be7aef3b-4414-4dd5-9ece-6a3f30e80c4f)
<br>
<br>

### v)Cut and paste portion of image:

##### Program:
```
import cv2
image=cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\nat.jpg')
image=cv2.resize(image,(300,300))
tag =image[150:200,110:160]
image[110:160,150:200] = tag
cv2.imshow('image1',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

<br>
<br>
<br>
<br>
<br>
<br>


## Output:

![image](https://github.com/SriSaiPriyaSenthilvel/COLOR_CONVERSIONS_OF-IMAGE/assets/119475702/5b808296-4dc5-45e2-8d69-a696585d0be5)

<br>
<br>

### vi) BGR and RGB to HSV and GRAY:

##### Program:
```
import cv2
img = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\nat.jpg')
img = cv2.resize(img,(200,200))
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
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>


## Output:
![image](https://github.com/SriSaiPriyaSenthilvel/COLOR_CONVERSIONS_OF-IMAGE/assets/119475702/e631a975-bb21-4b36-8d0e-df6eaf4ab4bd)

<br>
<br>

### vii) HSV to RGB and BGR:

##### Program:
```
import cv2
img = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\nat.jpg')
img = cv2.resize(img,(200,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>



## Output:
![image](https://github.com/SriSaiPriyaSenthilvel/COLOR_CONVERSIONS_OF-IMAGE/assets/119475702/1f6bddb3-1b57-4e8d-b3bc-ac84208caca6)

<br>
<br>

### viii) RGB and BGR to YCrCb:

##### Program:
```
import cv2
img = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\nat.jpg')
img = cv2.resize(img,(200,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

<br>
<br>
<br>
<br>
<br>
<br>


## Output:
![image](https://github.com/SriSaiPriyaSenthilvel/COLOR_CONVERSIONS_OF-IMAGE/assets/119475702/f7c9242d-19f1-43b0-840f-0de03a824f8c)

<br>
<br>

### ix) Split and merge RGB Image:

##### Program:
```
import cv2
img = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\nat.jpg')
img = cv2.resize(img,(200,200))

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
![image](https://github.com/SriSaiPriyaSenthilvel/COLOR_CONVERSIONS_OF-IMAGE/assets/119475702/358132e4-b6ba-4f21-a9fa-5e1eff487598)

<br>
<br>


### x) Split and merge HSV Image:

##### Program:
```
import cv2
img = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\nat.jpg')
img = cv2.resize(img,(200,200))
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

![image](https://github.com/SriSaiPriyaSenthilvel/COLOR_CONVERSIONS_OF-IMAGE/assets/119475702/7b4de0b2-7f08-4136-a4bc-ce1538fc0dd5)

<br>
<br>

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.
