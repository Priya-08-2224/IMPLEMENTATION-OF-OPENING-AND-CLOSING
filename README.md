# OPENING--AND-CLOSING
### Name - PRIYADHARSHINI J
### Register Number - 212224230210
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation
 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create a blank image

image = np.zeros((500, 500, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'AJAY', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

# Create the structuring element
kernel = np.ones((3, 3), np.uint8)

# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')


# Opening is erosion followed by dilation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

# Display the result of Opening
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')




# Closing is dilation followed by erosion
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
# Display the result of Opening
plt.imshow(cv2.cvtColor(closed_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Closing Operation")
plt.axis('off')

```
## Output:

### Display the input Image
<img width="952" height="611" alt="Screenshot 2026-05-16 225411" src="https://github.com/user-attachments/assets/35248ad5-dc8b-4aa6-bdf1-79654dda22b5" />




### Display the result of Opening
<img width="932" height="533" alt="Screenshot 2026-05-16 225417" src="https://github.com/user-attachments/assets/5294d5ad-0fca-4144-8920-5ae4c6a42c6e" />



### Display the result of Closing
<img width="932" height="533" alt="Screenshot 2026-05-16 225417" src="https://github.com/user-attachments/assets/08139454-3c9b-4399-ac1b-6b64896c4f54" />




<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
