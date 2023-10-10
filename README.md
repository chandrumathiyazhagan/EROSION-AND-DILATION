# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages to do Erosion and Dilution.
### Step2:
Create the text image of our name using putText from cv2 package.
### Step3:
Create the required structural element.
### Step4:
Apply Erode and Dilution for our NameImage.
### Step5:
Display the output images.
### step6:
End the programm
## Program:
### Import the necessary packages
``` Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
``` Python
image= np.zeros((100,600),dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image,'MK CHANDRU',(5,70), font,2,(255),5,cv2.LINE_AA)
cv2.imshow("Original",image)
```
### Create the structuring element
``` Python
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
### Erode the image
``` Python
erodeImage = cv2.erode(image,kernel1)
cv2.imshow("Eroded Image",erodeImage)
```
### Dilate the image
``` Python
dilationImage = cv2.dilate(image,kernel1)
cv2.imshow("Dilated Image",dilationImage)
```
``` Python
cv2.waitKey(0)
cv2.destoryAllWindows
```
## Output:

### Display the input Image
![Screenshot from 2023-10-10 14-45-46](https://github.com/chandrumathiyazhagan/EROSION-AND-DILATION/assets/119393023/330a29b3-58cf-41d4-af75-db75564e7391)

### Display the Eroded Image
![Screenshot from 2023-10-10 14-46-07](https://github.com/chandrumathiyazhagan/EROSION-AND-DILATION/assets/119393023/9338a9ac-b272-40a1-8324-88723898960c)

### Display the Dilated Image
![Screenshot from 2023-10-10 14-46-26](https://github.com/chandrumathiyazhagan/EROSION-AND-DILATION/assets/119393023/05b7f4fe-b65a-485f-9c35-5c33cdf8a1b5)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
