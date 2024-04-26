## OPENING--AND-CLOSING
### Aim
To implement Opening and Closing using Python and OpenCV.

### Software Required
1. Anaconda - Python 3.7
2. OpenCV
### Algorithm:
#### Step1:
Import the necessary packages
#### Step2:
Create the Text using cv2.putText
#### Step3:
Create the structuring element
#### Step4:
Use Opening operation
#### Step5:
Use Closing Operation

### Program:
```
Developed by: NAGUL K
Register Number:212222230089
```
#### Display the input Image
```
import cv2
import numpy as np

img = np.zeros((350, 1400), dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'N A G U L', (15, 200), font, 5, (255), 10, cv2.LINE_AA)
cv2.imshow('created_text', img)
cv2.waitKey(0)
```
#### Create ths structured element
```
struct_ele = np.ones((9, 9), np.uint8)
```
#### Display the result of Opening
```
opening = cv2.morphologyEx(img, cv2.MORPH_OPEN, struct_ele)
cv2.imshow('Opening', opening)
cv2.waitKey(0)
```
#### Display the result of Closing
```
closing = cv2.morphologyEx(img, cv2.MORPH_CLOSE, struct_ele)
cv2.imshow('Closing', closing)
cv2.waitKey(0)
```
### Output:

#### Display the input Image
![image](https://github.com/Nagul71/OPENING--AND-CLOSING/assets/118661118/7be183e7-7dfc-4805-8c40-0489c728d61c)





#### Display the result of Opening

![image](https://github.com/Nagul71/OPENING--AND-CLOSING/assets/118661118/77cf79eb-fa17-4c99-9016-f2e860e587f8)


#### Display the result of Closing
![image](https://github.com/Nagul71/OPENING--AND-CLOSING/assets/118661118/2a72b0e4-4831-4210-b4fc-501d0684c047)





### Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
