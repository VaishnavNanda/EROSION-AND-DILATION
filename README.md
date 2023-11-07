##  EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.
<br>


### Step2:
Create the text image using cv2.putText.
<br>

### Step3:
Then create the structuring image for dilation/erosion.
<br>

### Step4:
Apply erosion and dilation using plt.erode and plt.dilate.
<br>

### Step5:
Plot the images using plt.imshow.
<br>

 
## Program:


# Import the necessary packages:
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```



# Create the Text using cv2.putText:
```
image = np.zeros((100,500),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image,"S VAISHNAV NANDA",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(image,cmap='gray')
plt.title('Input Text'), plt.xticks([]), plt.yticks([])
plt.show()
```



# Create the structuring element:
```
kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```



# Erode the image:
```
image_erode=cv2.erode(image,kernel)
plt.imshow(image_erode,cmap='gray')
plt.title('Eroded Text'), plt.xticks([]), plt.yticks([])
plt.show()
```




# Dilate the image:
```
image_dilate=cv2.dilate(image,kernel)
plt.imshow(image_dilate,cmap='gray')
plt.title('Dilated Text'), plt.xticks([]), plt.yticks([])
plt.show()
```





## Output:

### Display the input Image:
![Screenshot from 2023-11-07 13-58-38](https://github.com/VaishnavNanda/EROSION-AND-DILATION/assets/118707051/5daf996d-8a77-44c6-9422-c8001b3f9075)


<br>
<br>
<br>
<br>
<br>
<br>

### Display the Eroded Image:
![Screenshot from 2023-11-07 13-58-49](https://github.com/VaishnavNanda/EROSION-AND-DILATION/assets/118707051/582038c4-5243-4f9e-bd13-512c8fd4e457)


<br>
<br>
<br>
<br>
<br>
<br>

### Display the Dilated Image:
![Screenshot from 2023-11-07 13-58-56](https://github.com/VaishnavNanda/EROSION-AND-DILATION/assets/118707051/f605ecd0-6c10-47f2-a6d8-5877f3aa1186)




<br>
<br>
<br>
<br>
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
