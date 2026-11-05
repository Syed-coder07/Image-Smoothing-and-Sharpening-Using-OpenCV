## Image-Smoothing-and-Sharpening-Using-OpenCV

## Aim:

To write a Python program using OpenCV to apply different smoothing filters (Averaging, Weighted Averaging, Gaussian, Median) and sharpening filters (Laplacian Kernel and Laplacian Operator) for image enhancement, and display each result separately along with the original image for comparison.

The program performs the following operations:
* Read and display an input image
* Apply Averaging filter
* Apply Weighted Averaging filter
* Apply Gaussian filter
* Apply Median filter
* Apply Laplacian sharpening using kernel
* Apply Laplacian operator
* Display all outputs for comparison

## Software Used:

* Anaconda – Python 3.7
* Jupyter Notebook / VS Code
* OpenCV (cv2)
* NumPy
* Matplotlib


## Algorithm:

## Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

## Step 2:
Read the input image (e.g., image.jpg).

## Step 3:
Convert the image from BGR to RGB format for display.

## Step 4:
Apply Averaging Filter using cv2.blur().

## Step 5:
Apply Weighted Averaging Filter using a custom kernel with cv2.filter2D().

## Step 6:
Apply Gaussian Filter using cv2.GaussianBlur().

## Step 7:
Apply Median Filter using cv2.medianBlur().

## Step 8:
Apply Laplacian Sharpening using Kernel with cv2.filter2D().

## Step 9:
Convert image to grayscale and apply Laplacian Operator using cv2.Laplacian().

## Step 10:
Display all filtered images using a grid layout for comparison.

## Program:

## Developed By: Syed Shamsheer Ali .B

## Register No: 212225220114

```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1 = cv2.imread(r"C:\Users\syedf\OneDrive\Documents\DIPT\Syed1.png")

if image1 is None:
    print("Error: Unable to load image. Check the file path.")
else:
    image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)
    kernel = np.ones((11, 11), np.float32) / 121
    image3 = cv2.filter2D(image2, -1, kernel)
    plt.figure(figsize=(12, 6))
    plt.subplot(1, 2, 1)
    plt.imshow(image2)
    plt.title("Original Image")
    plt.axis("off")
    plt.subplot(1, 2, 2)
    plt.imshow(image3)
    plt.title("Average Filtered Image")
    plt.axis("off")
    plt.show()
```

```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```

```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```

```
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```

```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```

```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```

## Output:

## Smoothing Filters:

## Display Original Image and Average Filtered Image:

<img width="1106" height="636" alt="image" src="https://github.com/user-attachments/assets/b5fd3eba-bc7a-41a6-9a4b-9ffabd4b94fa" />

## Display Original Image and Weighted Average Filtered Image:

<img width="651" height="411" alt="image" src="https://github.com/user-attachments/assets/3d4f62ef-0631-4e2d-9746-5a37432cb58f" />

## Display Original Image and Gaussian Blur Image:

<img width="643" height="413" alt="image" src="https://github.com/user-attachments/assets/786741d2-d24f-4a12-88a1-cdaa20f2ff24" />

## Display Original Image Median Blur Image:

<img width="877" height="553" alt="image" src="https://github.com/user-attachments/assets/49a38727-f64d-4f8b-81d5-9bf98ce05fc0" />

## Sharpening Filters:

## Display Original Image and Laplacian Kernel Image:

<img width="642" height="407" alt="image" src="https://github.com/user-attachments/assets/c78a4259-f0b4-4236-a181-1b0878f402c7" />

## Display the Original Image and Laplacian Operator Image:

<img width="630" height="397" alt="image" src="https://github.com/user-attachments/assets/ab71ee02-43b3-49b4-9cb7-fabc378623d2" />


## Result:

Thus, smoothing filters and sharpening filters are successfully implemented using OpenCV.

The smoothing filters reduce noise and improve image quality, while sharpening filters enhance edges and details for better feature extraction.







