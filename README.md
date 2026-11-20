# Image Segmentation Using Thresholding Techniques in OpenCV

## Aim

To segment an image using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques using Python and OpenCV.

The program performs the following operations:

- Global Thresholding
- Adaptive Thresholding
- Otsu's Thresholding

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Load the input image using OpenCV.

### Step 3:

Convert the input image into grayscale format.

### Step 4: Global Thresholding

- Select a fixed threshold value.
- Apply thresholding to separate foreground and background pixels.
- Display the thresholded image.

### Step 5: Adaptive Thresholding

- Compute threshold values for small regions of the image.
- Apply Adaptive Mean Thresholding.
- Apply Adaptive Gaussian Thresholding.
- Display the segmented images.

### Step 6: Otsu's Thresholding

- Automatically determine the optimal threshold value.
- Apply Otsu's thresholding technique.
- Display the segmented image.

### Step 7:

Compare the results obtained from Global, Adaptive, and Otsu's thresholding methods.

## Program

## Developed By

**Name: Bhuvanesh.K** 

**Register No:212225230035** 

## Output

### Original Image
```
import cv2
import matplotlib.pyplot as plt

img = cv2.imread("baseball.jpg")

if img is None:
    print("Error: Image not found. Check the file path.")
else:
    img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
    plt.imshow(img_rgb)
    plt.title("Original Image")
    plt.axis("off")
    plt.show()
```

<img width="803" height="550" alt="image" src="https://github.com/user-attachments/assets/03f7b219-8093-496b-bb1d-f2447aa556cf" />

### ORIGINAL grayscale image
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("baseball.jpg", cv2.IMREAD_GRAYSCALE)
plt.imshow(img, cmap="gray")
plt.title("Original Grayscale Image")
plt.axis("off")
plt.show()
```
<img width="792" height="542" alt="image" src="https://github.com/user-attachments/assets/5dfa310b-2cf3-499a-a30b-702a69c011ed" />

### Global Thresholding

```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("baseball.jpg", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(img, 127, 255, cv2.THRESH_BINARY)
plt.imshow(result, cmap="gray")
plt.title("Global Thresholding")
plt.axis("off")
plt.show()
```
<img width="805" height="555" alt="image" src="https://github.com/user-attachments/assets/a751949b-3a20-4141-89d7-80074ca84762" />

### Adaptive Thresholding

```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("baseball.jpg", cv2.IMREAD_GRAYSCALE)
result = cv2.adaptiveThreshold(
    img, 255,
    cv2.ADAPTIVE_THRESH_GAUSSIAN_C,
    cv2.THRESH_BINARY,
    11, 2
)
plt.imshow(result, cmap="gray")
plt.title("Adaptive Thresholding")
plt.axis("off")
plt.show()
```
<img width="802" height="547" alt="image" src="https://github.com/user-attachments/assets/432fb6a6-8b1f-4d74-a515-6fae096b6472" />

### Otsu's Thresholding

```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("baseball.jpg", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(
    img, 0, 255,
    cv2.THRESH_BINARY + cv2.THRESH_OTSU
)
plt.imshow(result, cmap="gray")
plt.title("Otsu's Thresholding")
plt.axis("off")
plt.show()
```
<img width="793" height="540" alt="image" src="https://github.com/user-attachments/assets/d75385f8-6fb3-4967-ac8d-279277cda5cf" />


## Result

Thus, image segmentation is successfully performed using **Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding** techniques in OpenCV. 
