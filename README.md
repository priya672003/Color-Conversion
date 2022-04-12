# Color Conversion
## AIM:
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:

Import cv2 library and upload the image or capture an image.

### Step2:

Read the saved image using cv2.imread("filename.jpg").

### Step3:

Convert the image into the given color transformation using cv2.cvtColor(image, cv2.BGR2YCrCb) and similarly for other color formats.

### Step4:

Split and merge the image using cv2.split(hsv) and cv2.merge([h,s,v])

### Step5:

Output the image using cv2.imshow("OUTPUT", image)

## Program:
## Developed By: PRIYADARSHINI R
## Register Number: 212220230038
# i) Convert BGR and RGB to HSV and GRAY
```python


import cv2
house_color_image = cv2.imread("pic.jpg")
cv2.imshow('212220230024',house_color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

hsv_image = cv2.cvtColor(house_color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv_image)

hsv_image1 = cv2.cvtColor(house_color_image, cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()

gray_image = cv2.cvtColor(house_color_image, cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray_image)

gray_image1 = cv2.cvtColor(house_color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()



```
# ii)Convert HSV to RGB and BGR
```python


RGB_image = cv2.cvtColor(house_HSV_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV TO RGB',RGB_image)

BGR_image = cv2.cvtColor(house_HSV_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV TO BGR',BGR_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
# iii)Convert RGB and BGR to YCrCb
```python


YCrCb_image = cv2.cvtColor(house_color_image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB to YCrCb',YCrCb_image)

YCrCb_image1 = cv2.cvtColor(house_color_image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR to YCrCb',YCrCb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
# iv)Split and Merge RGB Image
```python


blue = RGB_image[:,:,0]
green = RGB_image[:,:,1]
red = RGB_image[:,:,2]
cv2.imshow("R plane",red)
cv2.imshow("G plane",green)
cv2.imshow("B plane",blue)
p=cv2.merge((blue,green,red))
cv2.imshow("merged",p)
cv2.waitKey(0)
cv2.destroyAllWindows()



```
# v) Split and merge HSV Image
```python


h, s, v = cv2.split(hsv_image)
cv2.imshow("h plane",h)
cv2.imshow("s plane",s)
cv2.imshow("v plane",v)
merged = cv2.merge((h,s,v))
cv2.imshow("merge",merged)
cv2.waitKey(0)
cv2.destroyAllWindows()



```
## Output:
### i) BGR and RGB to HSV and GRAY

![img1](https://user-images.githubusercontent.com/81132849/162880624-22e90e50-86e2-49f5-9f8d-a5a17d2a93de.png)
![img2](https://user-images.githubusercontent.com/81132849/162880640-884e9f43-210f-4627-b460-9ebc0ff19dc2.png)


### ii) HSV to RGB and BGR

![img3](https://user-images.githubusercontent.com/81132849/162880769-ffb9368d-4b1b-4d1c-a925-3d3fa24cbee6.png)


### iii) RGB and BGR to YCrCb

![img4](https://user-images.githubusercontent.com/81132849/162880950-954e9ac3-c560-491d-b286-b1cbb856b50f.png)


### iv) Split and merge RGB Image

![img5](https://user-images.githubusercontent.com/81132849/162880986-0d99360c-7b0c-4c4e-bba4-12747b24ea16.png)
![img6](https://user-images.githubusercontent.com/81132849/162881003-271d862e-364c-413a-8863-06e7affb689e.png)


### v) Split and merge HSV Image

![img7](https://user-images.githubusercontent.com/81132849/162881071-3124ee56-6600-4659-8a8a-85bd83b62ce2.png)
![img8](https://user-images.githubusercontent.com/81132849/162881342-dc2290f5-8593-409b-af74-04a0343b00ff.png)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
