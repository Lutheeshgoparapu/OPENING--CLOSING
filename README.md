# OPENING--CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

Step 1 : Import the necessary packages.

Step 2 : Create the Text using cv2.putText

Step 3 : Create the structuring element.

Step 4 : Use Opening operation.

Step 5 : Use Closing Operation.
 
## Program:

```
Developed BY : G Lutheesh
Reg No : 212221230029
```
```




# Import the necessary packages :

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText :

img=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'LUTHEESH',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img)
plt.show()

# Create the structuring element :

kernel=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

# Use Opening operation :

image_open=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.axis('off')
plt.imshow(image_open)
plt.show()

# Use Closing Operation :

image_close=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.axis('off')
plt.imshow(image_close)
plt.show()



```
## Output:

### Display the input Image
![WhatsApp Image 2023-10-25 at 11 19 45_5884eb52](https://github.com/Lutheeshgoparapu/OPENING--CLOSING/assets/94154531/bb2e435e-00be-4032-8063-6669f94afa95)


### Display the result of Opening
![WhatsApp Image 2023-10-25 at 11 19 53_3549cd4d](https://github.com/Lutheeshgoparapu/OPENING--CLOSING/assets/94154531/8aae61c0-7e8a-499a-afa7-a6fdc6ab1a76)


### Display the result of Closing
![WhatsApp Image 2023-10-25 at 11 20 16_6a76635e](https://github.com/Lutheeshgoparapu/OPENING--CLOSING/assets/94154531/99f17fa9-1168-4429-9831-735dbb00cf99)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
