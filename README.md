# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
Step 1: Import the necessary packages.

Step 2: Create the Text using cv2.putText.

Step 3: Create the structuring element.

Step 4: Use Opening operation.

Step 5: Use Closing Operation.

Step 6: Print the output and end the program.

 
## Program:

```
# Import the necessary packages

import numpy as np
import matplotlib.pyplot as plt
import cv2

# Create the Text using cv2.putText

text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image," sameer",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image)
plt.axis('off')

# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation

opening_image = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(opening_image)
plt.axis('off')

# Use Closing Operation

closing_image = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(closing_image)
plt.axis('off')



```
## Output:
### Display the input Image
![11 1](https://user-images.githubusercontent.com/93427186/172909197-9cf5ca8d-5e27-4970-8808-b9664025949d.png)
### Display the result of Opening
![11 2](https://user-images.githubusercontent.com/93427186/172909210-a7351112-153e-4f0d-ae09-522af5f1e15d.png)
### Display the result of Closing
![11 3](https://user-images.githubusercontent.com/93427186/172909274-927f6755-c7b2-4061-8167-db269dc47ed6.png)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
