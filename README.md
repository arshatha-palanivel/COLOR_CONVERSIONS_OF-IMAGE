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
Convert BGR and RGB to HSV and GRAY.
### Step7:
Convert HSV to RGB and BGR.
### Step8:
Convert RGB and BGR to YCrCb.
### Step9:
Split and Merge RGB Image.
### Step10:
Split and merge HSV Image.

##### Program:
### Developed By: ARSHATHA P
### Register Number: 212222230012


## Output:

### i) Read and display the image
```
    import cv2
    image=cv2.imread('dip.jpg',1)
    image=cv2.resize(image,(300,300))
    cv2.imshow('ARSHATHA P',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()

  ```
![DIP 01](https://github.com/arshatha-palanivel/COLOR_CONVERSIONS_OF-IMAGE/assets/118682484/30fe1927-b23d-4030-bb81-7223f814d8a9)



### ii)Write the image
```
    import cv2
    image=cv2.imread('dip.jpg',0)
    cv2.imwrite('demos.jpg',image)

   ``` 
![DIP 02](https://github.com/arshatha-palanivel/COLOR_CONVERSIONS_OF-IMAGE/assets/118682484/161b1a64-8764-40b2-816b-94ff2a75f30d)



### iii)Shape of the Image
```
    import cv2
    image=cv2.imread('dip.jpg',1)
    print(image.shape)
```

![DIP 03](https://github.com/arshatha-palanivel/COLOR_CONVERSIONS_OF-IMAGE/assets/118682484/848a4d07-8197-4d68-834f-4be8902c2a90)



### iv)Access rows and columns
```
    import random
    import cv2
    image=cv2.imread('dip.jpg',1)
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
   ![DIP 04](https://github.com/arshatha-palanivel/COLOR_CONVERSIONS_OF-IMAGE/assets/118682484/3b8ac2ff-ab9d-4b03-b090-4302530390af)

    


### v)Cut and paste portion of image
```
 import cv2
  image=cv2.imread('dip.jpg',1)
  image=cv2.resize(image,(300,300))
  tag =image[150:200,110:160]
  image[110:160,150:200] = tag
  cv2.imshow('image1',image)
  cv2.waitKey(0)
  cv2.destroyAllWindows()
```
  ![DIP 05](https://github.com/arshatha-palanivel/COLOR_CONVERSIONS_OF-IMAGE/assets/118682484/3a73b3fb-f389-4923-b25a-8315d0e480d5)


### vi) BGR and RGB to HSV and GRAY
```
import cv2
img = cv2.imread('dip.jpg',1)
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
![DIP 06](https://github.com/arshatha-palanivel/COLOR_CONVERSIONS_OF-IMAGE/assets/118682484/946dc39b-c290-4a47-b6c6-4fce07a700b1)


### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread('dip.jpg')
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
![DIP 07](https://github.com/arshatha-palanivel/COLOR_CONVERSIONS_OF-IMAGE/assets/118682484/693febcb-d3e8-4e88-802d-a78b6dfd54ec)


### viii) RGB and BGR to YCrCb
```
import cv2
img = cv2.imread('dip.jpg')
img = cv2.resize(img,(200,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![DIP 08](https://github.com/arshatha-palanivel/COLOR_CONVERSIONS_OF-IMAGE/assets/118682484/946e10d4-d772-4ffc-8299-bb9f6ca9c9d4)



### ix) Split and merge RGB Image
```
import cv2
img = cv2.imread('dip.jpg',1)
img = cv2.resize(img,(150,150))

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
![DIP 09](https://github.com/arshatha-palanivel/COLOR_CONVERSIONS_OF-IMAGE/assets/118682484/e0856887-ef80-4d82-807e-120bebd236de)



### x) Split and merge HSV Image
```
import cv2
img = cv2.imread("dip.jpg",1)
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
![DIP 10](https://github.com/arshatha-palanivel/COLOR_CONVERSIONS_OF-IMAGE/assets/118682484/6a0cdba9-9fe5-4d76-875a-708ab593231c)




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







