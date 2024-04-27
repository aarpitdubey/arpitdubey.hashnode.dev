---
title: "From Pixels to Pathways: The Magical Eyes"
seoTitle: "lane detection, self-driving cars, object detection, computer vision"
datePublished: Sat Apr 27 2024 09:40:37 GMT+0000 (Coordinated Universal Time)
cuid: clvhwvf39001d0al6bngfamwk
slug: from-pixels-to-pathways-the-magical-eyes
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1714210523748/c32c1d97-016f-4050-b627-942e76f6eab6.gif
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1714210642438/e9ea5423-423c-42c7-a59b-bce3e16b0953.gif
tags: computer-vision, udacity, object-detection, udacitynanodegree, self-driving-car, lane-detection, lane-line-detectio

---

*“Self-driving cars are the natural extension of active safety and obviously something we should do.”* ~**Elon Musk**

## Introduction to lane line Detection:

When you and I drive a car, we rely on our eyes to see where the lane lines are. But cars don't have eyes, so computer vision technology steps in to assist. By utilizing intricate algorithms, computers can interpret their surroundings just like we do, allowing them to navigate the world effectively.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714140455894/ba2eae9b-4390-4869-9b06-dcb14d878693.png align="center")

When we applied the computer vision algorithm to an image or video, the car was able to detect the lane lines itself using cameras or other sensors.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714140376302/a814e29d-f7ca-464f-b5c8-941237f568ca.gif align="center")

finding the lane lines in the series of camera images or camera frames.

### Finding and identifying lane lines is our task:

Here, we have an image of lane lines below:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714142441719/832862c5-4ecf-43e7-87f8-a8cd5c55b5c7.jpeg align="center")

We can easily see the lane lines, but our goal is to make them detectable to the cameras, so our algorithm can identify them.

**Step 1**: Create a directory/folder name `self_driving_car` and inside it a folder named `computer-vision` and inside it another directory named `finding-lanes` then create a Python file named `lanes.py` and try to show this above image using the `cv` library. let's do this first step.

```bash
mkdir self_driving_car
cd self_driving_car

mkdir computer-vision
cd computer-vision

mkdir finding-lanes
cd finding-lanes
code .
```

When you are inside the `finding-lanes` folder creates a Python file named `lanes.py` and a folder named `images` and save the above lane image file.

In `lanes.py` file using two OpenCV methods `imread`() and `imshow()` methods we can able to read and show the images.

```python
import cv2
image = cv2.imread('./images/test_image.jpg')
cv2.imshow('result', image)
cv2.waitKey(0)
```

* Importing the OpenCV library
    

```python
import cv2
```

This line imports the OpenCV library in Python, which is widely used for computer vision and image-processing tasks.

* Reading an image
    

```python
image = cv2.imread('./images/test_image.jpg')
```

Here, the `cv2.imread()` function is used to read an image file named "test\_image.jpg" located in the "./images" directory relative to the current location of the script. The function reads the image and stores it in the variable named `image`.

* Displaying the image
    

```python
cv2.imshow('result', image)
```

The `cv2.imshow()` function is used to display the image read in the previous step. The first argument is a string title for the window, and the second argument is the image variable, which contains the image data.

* Wait for User Input
    

```python
cv2.waitKey(0)
```

This line of code waits indefinitely for a keyboard event. The argument passed to `cv2.waitKey()` specify the time (in milliseconds) the window should wait for a keyboard event. In this case, `0` signifies that the window will wait indefinitely until any key is pressed.

**Step 2: Applying the canny edge detection technique**

The goal of edge detection is to identify the boundaries of objects within images. in essence, we'll be using detection to try and find regions in an image where there is a sharp change in intensity (or) a sharp color change.

**Edge Detection:** Identifying sharp changes in intensity in adjacent pixels.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714155719825/8dcf902f-46b7-4f37-ad94-76988d0b9390.png align="center")

An image can mirror it as a **matrix**, an array of pixels, a pixel contains the light intensity at some location in the image. each pixel intensity is denoted by a numeric value that ranges from **0 to 255** and an intensity value of zero indicates no intensity.

It is completely black where values are 255 represent maximum intensity, and completely white where values are 0.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714156109900/32789724-9996-4537-9070-3f8f4372cb18.png align="center")

Here comes the gradient, which is the change in brightness over a series of pixels.

**Gradient:** Measure of change in brightness over adjacent pixels.

A **strong gradient** indicates a **steep** change whereas, a **small gradient** represents a **shallow** change.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714156493409/6c511512-157d-48bb-9abc-08d4c67a8791.png align="center")

Let's understand this concept using an example of a soccer ball. Below is the image given.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714156628620/4fb01dd8-27f4-43c8-9e42-3516c3860ce3.png align="center")

On the right-hand side of the image, you can see the gradient of the soccer ball. The white pixels indicate a sudden change in brightness which occurs at the points of the strengthened gradient. These bright pixels help us identify edges in our image.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714157345296/6f3914d1-96f5-4655-8b55-5c758e86d8a7.gif align="center")

An edge is defined by the difference in intensity values in adjacent pixels. Whenever there is a sharp change in intensity or a rapid change in brightness, we observe a strong gradient and a corresponding bright pixel in the gradient image. By tracing out all of these bright pixels, we can obtain the edges of the image.

* **Convert the lane image into grayscale:** images are made up of pixels, A three-channel color image would have Red, Green, and Blue channels hence each pixel is a combination of three intensities values whereas, a grayscale image only has one channel for each pixel with one intensity value or one channel ranging from 0 to 255.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714157737338/f2154b1d-3753-4ebc-ba9c-e26cd9ef6561.png align="center")

**The point is that using grayscale image processing with a single channel is faster and less computationally intensive than processing a three-channel color image.**

```python
import cv2
import numpy as np

image = cv2.imread('./images/test_image.jpg')
lane_image = np.copy(image)
gray_lane_image = cv2.cvtColor(lane_image, cv2.COLOR_BGR2GRAY)

cv2.imshow('result', gray_lane_image)
cv2.waitKey(0)
```

* `cv2.imread()` reads the image file "test\_image.jpg" from the specified path and stores it in the variable `image`.
    
* `np.copy()` is used to create a new copy of the image stored in the variable `image`. This ensures that any modifications made to the `lane_image` variable do not affect the original `image`.
    
* `cv2.cvtColor()` converts the color image stored, `lane_image` into a grayscale image. The function takes two arguments: the source image and the conversion code, `cv2.COLOR_BGR2GRAY`, which specifies the color space conversion.
    
* `cv2.imshow()` displays the grayscale image. The first argument is a string title for the window, and the second argument is the grayscale image variable, `gray_lane_image`.
    
* `cv2.waitKey(0)` waits indefinitely for a keyboard event. The argument `0` specifies the time (in milliseconds) the window should wait for a keyboard event. Here, it waits indefinitely until any key is pressed.
    
    **Converting the Image to Grayscale and Displaying**
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714158306504/a7f1e81a-5393-4125-97a9-6339b8bc3a0d.png align="center")

* **Reducing noise and smoothening our image by applying Gaussian blur:** When detecting edges we must filter out any image noise because image noise can create false edges and ultimately affect edge detection that's why it is imperative to filter it out and thus, smoothen the image.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714159045980/70281b45-714e-4333-bd89-d3a1960aec82.png align="center")

Filtering out image noise and smoothening will be done with a Gaussian filter. The image is a collection of discrete pixels. Each of the pixels for a grayscale image is represented by a single number that describes the brightness of the pixel.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714159187528/f7ca009c-76cb-4be1-85c8-1dfad91baba3.png align="center")

To smoothen the image, we have to **modify the value of a pixel with the average of the pixel intensity around it.** Averaging out the pixels in the image to reduce noise will be done with the **kernel**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714168146862/0bd460a3-7338-47e5-802c-2f16e0037838.gif align="center")

Essentially, this kernel of normally distributed numbers runs across our entire image and sets each pixel value to about the weighted average of its neighboring pixels, smoothing out the image.

```python
import cv2
import numpy as np

image = cv2.imread('./images/test_image.jpg')
lane_image = np.copy(image)
gray = cv2.cvtColor(lane_image, cv2.COLOR_BGR2GRAY)
# Added to smoothening and reducing noise in image
blur = cv2.GaussianBlur(gray, (5, 5), 0)

cv2.imshow('With Gaussian blur', blur)
cv2.waitKey(0)
```

**step 3: Applying Gaussian Blur**

The `cv2.GaussianBlur()` function is used to apply Gaussian blur to the grayscale image. This is achieved to reduce noise and smoothen the image, which can be beneficial for subsequent image-processing tasks

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714168847884/6fd31ed8-efed-425e-b7c8-c9400f2c2e44.png align="center")

So let's see both images before applying Gaussian blur and with Gaussian blur:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714169357003/b6fe61e4-8370-466f-84ca-1787e5599700.png align="center")

* **Applying the Canny Edge detection method:** It helps to find **edges** in our image, **an edge corresponds to a region in an image** where there is a sharp change in intensity (or) a sharp change in color between adjacent pixels in the image. The **change in brightness over a series of pixels** is the gradient. Strong gradient. A strong gradient indicates a steep change whereas a small gradient indicates a shallow change.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714173686226/eccaf03e-b5b1-43d8-b310-67a68721ba7a.png align="center")
    
    Images consist of pixels and can be interpreted as a matrix or an array of pixel intensities for calculating gradients in an image. Additionally, the i**mage can be represented in a 2D coordinate space (X, Y)**, where the x-axis traverses the image and the y-axis corresponds to the image height, representing the number of columns and rows in the image. This means that **the product of the width and height gives the total number of pixels in the image**.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714174097751/d73f90ce-4f85-40d3-b30f-c5eaf808fe35.png align="center")
    
    The point is that we can view our image not only as an array but also as a **continuous function of x and y**. Being a mathematical function allows us to conduct mathematical operations.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714174276315/cae7107a-5808-4277-8dfc-fde471cb81cb.png align="center")
    
    So, which operator can we use to detect a quick change in the brightness of our image? The canny function calculates the derivative of our function in both the x and y directions, measuring the intensity change compared to neighboring pixels. A small derivative indicates a minor/small intensity change
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714174672049/caa8c146-fe74-4f5c-aba2-cc9486be4e5e.png align="center")
    
    while a large derivative indicates a big/significant change.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714174730763/787c4e3c-85a6-49a2-978e-42f3179748ee.png align="center")
    
    When we call the canny function it does all of that for us.
    
* **Canny Function:** It computes the gradient in all directions of our blurred image and then traces our strongest gradients as a series of white pixels.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714175032595/6813c550-0ca3-4236-bce0-eea2e6a99395.png align="center")
    
    ```python
    cv2.Canny(image, low_threshold, high_threshold)
    ```
    
    `low_threshold` and `high_threshold` are used to isolate adjacent pixels based on gradient strength.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714175656854/501506f6-3560-4436-ab18-543090a902a6.gif align="center")
    
    If the gradient is higher than, `high_threshold`it is considered an edge pixel; if it is below, `low_threshold` it is rejected. If the gradient is between both thresholds then it will be accepted only, if it is connected to a strong edge. The documentation itself, recommends using a ratio of 1:2 (or) 1:3 (or 50:150).
    
    ```python
    import cv2
    import numpy as np
    
    image = cv2.imread('./images/test_image.jpg')
    lane_image = np.copy(image)
    gray  = cv2.cvtColor(lane_image, cv2.COLOR_BGR2GRAY)
    blur  = cv2.GaussianBlur(gray, (5, 5), 0)
    canny = cv2.Canny(blur, 50, 150)
    
    cv2.imshow('Image after applying canny function', canny)
    cv2.waitKey(0)
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714176083066/a6facfcf-e609-48db-ba61-c4efb0091d82.png align="center")
    
    Here is the gradient image which clearly outlines the edges corresponding to the sharpest changes in intensity gradients. Pixels exceeding the `high_threshold` are **traced as bright**, identifying adjacent pixels with the most rapid changes in brightness. Small changes below the `low_threshold` remain **untraced** and appear black.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714176124281/51c917db-644c-45ae-b241-59bee741ca10.png align="center")
    
    **Step 4: Find the region of interest and** `bitwise_and()` **to the image**
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714176858429/030e21cd-90b3-434c-b9ed-a3aa2e505fa3.png align="center")
    
    let's structure the code in a modular format and show the image using Matplotlib.
    
* ```python
      import cv2
      import numpy as np
      import matplotlib.pyplot as plt
      
      # user define function to perform grayscaling, noise reduction and canny 
      # in one function
      def canny(image):
          gray  = cv2.cvtColor(lane_image, cv2.COLOR_BGR2GRAY)
          blur  = cv2.GaussianBlur(gray, (5, 5), 0)
          canny = cv2.Canny(blur, 50, 150)
          return canny
          
      image = cv2.imread('./images/test_image.jpg')
      lane_image = np.copy(image)
      canny = canny(lane_image)
      
      plt.imshow(canny) # instead of cv2 using plt 
      plt.show()
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714177407137/90c47690-31e6-4b29-b81f-81f05af0c457.png align="center")
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714177635617/6562f811-2485-4ae6-926a-d28157cd9ea9.png align="center")
    

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

def canny(image):
    gray  = cv2.cvtColor(lane_image, cv2.COLOR_BGR2GRAY)
    blur  = cv2.GaussianBlur(gray, (5, 5), 0)
    canny = cv2.Canny(blur, 50, 150)
    return canny

def region_of_interest(image):
    height = image.shape[0]
    polygons = np.array([[(200, height), (1100, height), (550, 250)]])
    mask = np.zeros_like(image)
    cv2.fillPoly(mask, polygons, 255)
    return mask
    
image = cv2.imread('./images/test_image.jpg')
lane_image = np.copy(image)
canny = canny(lane_image)

cv2.imshow("Region Of Interest", region_of_interest(canny))
cv2.waitKey(0)
```

**Importing Libraries**

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

The code imports the necessary libraries, including `cv2` for computer vision operations, `numpy` for array manipulation, and `matplotlib.pyplot` for plotting images.

1. **<mark>Canny Edge Detection Function</mark>**
    
    ```python
    def canny(image):
        gray  = cv2.cvtColor(lane_image, cv2.COLOR_BGR2GRAY)
        blur  = cv2.GaussianBlur(gray, (5, 5), 0)
        canny = cv2.Canny(blur, 50, 150)
        return canny
    ```
    
    The `canny()` function is defined to take an input image and perform the following operations:
    
    * Convert the input image to grayscale using `cv2.cvtColor()`.
        
    * Apply Gaussian blur to the grayscale image using `cv2.GaussianBlur()`.
        
    * Perform Canny edge detection on the blurred image using `cv2.Canny()`.
        
    * Return the resulting Canny edges.
        
2. **<mark>Region of Interest Function</mark>**
    
    ```python
    def region_of_interest(image):
        height = image.shape[0]
        polygons = np.array([[(200, height), (1100, height), (550, 250)]])
        mask = np.zeros_like(image)
        cv2.fillPoly(mask, polygons, 255)
        return mask
    ```
    
    * The `region_of_interest()` function defines a region of interest on the input image and creates a mask.
        
    * It calculates the height of the input image, defines a polygon to represent the region of interest, creates a mask of zeros with the same dimensions as the input image, fills the defined polygon with white (255), and returns the resulting mask.
        
3. **Image Processing**
    
    ```python
    image = cv2.imread('./images/test_image.jpg')
    lane_image = np.copy(image)
    canny = canny(lane_image)
    ```
    
    * The code reads an image from the file "test\_image.jpg" and stores it in the variable `image`. The function `cv2.imread()` is used for this purpose.
        
    * The `np.copy()` function is used to create a copy of the original image, stored in the variable `lane_image`.
        
    * The `canny()` function is then called with `lane_image` as the input, and the resulting Canny edges are stored in the variable `canny`.
        
4. **Displaying the Masked Image**
    
    ```python
    cv2.imshow("Region Of Interest", region_of_interest(canny))
    cv2.waitKey(0)
    ```
    
    * The `region_of_interest()` function is called with the Canny edges as input to create a masked image.
        
    * The masked image is displayed in a window titled "Region Of Interest" using `cv2.imshow()`.
        
    * The `cv2.waitKey(0)` statement waits indefinitely for a keyboard event, allowing the user to view the displayed image until a key is pressed.
        

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714178457737/91de7683-952d-41de-871d-885ff85f21e1.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714178496721/5c9768f0-533d-4964-a3e5-05eced43216f.png align="center")

let's take the pixel representation of this resized image.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714183008284/d1f2a41e-155d-42d2-bbbb-4286ba3e1480.png align="center")

A triangular polygon translates to pixel intensities of 255 as white and the block surrounding region translates to pixel intensities of zeroes.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714183165072/4c071525-175a-4a62-96b9-6fd2bbf9b919.png align="center")

The binary representation of zero:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714183220121/50ff8525-9923-4bf9-974d-dac47b50b409.png align="center")

the binary representation of 255:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714183267907/b162a2c1-bbbe-47c0-8efd-1b2deeb82d3c.png align="center")

2<sup>7 </sup> \+ 2<sup>6 </sup> \+ 2<sup>5 </sup> \+ 2<sup>4 </sup> \+ 2<sup>3 </sup> \+ 2<sup>2 </sup> \+ 2<sup>1 </sup> \+ 2<sup>0 </sup> \= 255 \[1, 1, 1, 1, 1, 1, 1, 1\]. It is the maximum representable value by an 8-bit byte. So we conclude the surrounding region is completely black then, its binary representation is all zeroes \[0, 0, 0, 0, 0, 0, 0, 0\].

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714183674360/2b35c95e-f7a1-4dd2-bc85-0ade8b2299bc.png align="center")

We can apply the bitwise AND operation between the two images. The bitwise AND operation occurs element-wise between the two arrays of pixels.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714184089043/bd733413-0fbb-462d-8a73-8ee859d3e6b8.png align="center")

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

def canny(image):
    gray  = cv2.cvtColor(lane_image, cv2.COLOR_BGR2GRAY)
    blur  = cv2.GaussianBlur(gray, (5, 5), 0)
    canny = cv2.Canny(blur, 50, 150)
    return canny

def region_of_interest(image):
    height = image.shape[0]
    polygons = np.array([[(200, height), (1100, height), (550, 250)]])
    mask = np.zeros_like(image)
    cv2.fillPoly(mask, polygons, 255)
    masked_image = cv2.bitwise_and(image, mask)
    return masked_image
    
image = cv2.imread('./images/test_image.jpg')
lane_image = np.copy(image)
canny = canny(lane_image)
cropped_image = region_of_interest(canny)
cv2.imshow("Region Of Interest", cropped_image)
cv2.waitKey(0)
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714184119360/9ad826de-863a-4813-81a4-bf6be41a2552.png align="center")

**Step 5: Applying Hough transform**

The Hough transform is a technique used in image processing and computer vision to detect shapes, particularly lines and curves, within an image. Here's a simple explanation of the Hough transform:

1. **Basic Concept**: Imagine you have an image with a bunch of edge pixels that form a line. The Hough transform helps you find which straight line those edge pixels belong to.
    
    ```python
    import cv2
    
    # Creating an image with a line
    image = np.zeros((200, 200), dtype=np.uint8)
    cv2.line(image, (50, 50), (150, 150), 255, 1)
    
    cv2.imshow("Image with Line", image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
    ```
    
2. **Parameter Space**: The Hough transform works by representing lines in a different space called the "Hough space" or "parameter space." Instead of the usual x-y coordinates of a line, Hough space uses parameters like slope (m) and intercept (c) for a normal line equation (y = mx + c).
    
    ```python
    import numpy as np
    
    # Regular line equation: y = mx + c
    # Hough space: m - Slope, c - Intercept
    # Image to Hough Transform space conversion
    m = np.arange(-10, 10, 1)
    c = np.arange(0, 200, 1)
    
    # Visualizing Hough space
    M, C = np.meshgrid(m, c)
    
    print("Hough Space: ")
    print("Slope (m):", M)
    print("Intercept (c):", C)
    ```
    
3. **Voting Process**:
    
    * For each edge point in the image, the Hough transform "votes" for all possible lines that could pass through it in the Hough space.
        
    * Each edge point contributes to a curve in the Hough space, and the intersection of these curves indicates the parameters of the line that fits the edge points.
        
    
    ```python
    # Imaginary edge points
    edge_points = [(80, 75), (90, 85), (100, 95)]
    
    for point in edge_points:
        m = (point[1] - 50) / (point[0] - 50)  # Calculate slope
        c = point[1] - m * point[0]  # Calculate intercept
        print("Voting for line with slope m =", m, "and intercept c =", c)
    ```
    
4. **Accumulator Array**: This "voting" process is often visualized using an "accumulator array," which is a grid in the Hough space. Each cell in the grid accumulates votes for a particular line defined by its parameters.
    

```python
# Setting up accumulator array
accumulator = np.zeros((200, 200), dtype=np.uint8)

# Casting votes for the line: y = mx + c
for m, c in zip(m_vals, c_vals):
    y = np.round(m * x + c).astype(int)
    accumulator[y, x] += 1
```

**Finding Peaks**:

After all edge points have been voted, peaks in the accumulator array indicate the most likely parameters of the lines in the image.

These peaks correspond to the parameters of the lines that were "popular" among the edge points.

```python
# Find peaks in the accumulator array
peaks = cv2.HoughLines(accumulator, 1, np.pi / 180, threshold=50)

# Plotting the detected lines in the original image
for peak in peaks:
    rho, theta = peak[0]
    a = np.cos(theta)
    b = np.sin(theta)
    x0 = a * rho
    y0 = b * rho
    x1 = int(x0 + 1000 * (-b))
    y1 = int(y0 + 1000 * (a))
    x2 = int(x0 - 1000 * (-b))
    y2 = int(y0 - 1000 * (a)
    cv2.line(image, (x1, y1), (x2, y2), (0, 255, 0), 2)
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714185231608/260ea439-0a37-463a-a391-fbb90e67a6d6.png align="center")

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

def canny(image):
    gray  = cv2.cvtColor(lane_image, cv2.COLOR_BGR2GRAY)
    blur  = cv2.GaussianBlur(gray, (5, 5), 0)
    canny = cv2.Canny(blur, 50, 150)
    return canny

def display_lines(image, lines):
    line_image = np.zeros_like(image)
    if lines is not None:
        for line in lines:
            x1, y1, x2, y2 = line.reshape(4)
            cv2.line(line_image, (x1, y1), (x2, y2), (255, 0, 0), 10)
    return line_image
    
    
def region_of_interest(image):
    height = image.shape[0]
    polygons = np.array([[(200, height), (1100, height), (550, 250)]])
    mask = np.zeros_like(image)
    cv2.fillPoly(mask, polygons, 255)
    masked_image = cv2.bitwise_and(image, mask)
    return masked_image
    
image = cv2.imread('./images/test_image.jpg')
lane_image = np.copy(image)
canny = canny(lane_image)
cropped_image = region_of_interest(canny)
lines = cv2.HoughLinesP(cropped_image, 2, np.pi/180, 100, np.array([]), minLineLength=40, maxLineGap=5)
line_image = display_lines(lane_image, lines)

cv2.imshow("Region Of Interest", line_image)
cv2.waitKey(0)
```

* The `display_lines()` function takes the original image and detected lines as input.
    
* It creates a blank image of the same size as the input image and draws the detected lines on it using `cv2.line()`.
    
* The function then returns the image with the detected lines drawn on it.
    
* The Hough line transform is applied to the cropped image `cv2.HoughLinesP()` to detect the lines. Then, the detected lines are drawn on a separate image `display_lines()` and stored in `line_image`.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714185400495/85220bb8-fb4d-42fa-9e3a-1f4cfcc06112.png align="center")
    
    ```python
    import cv2
    import numpy as np
    import matplotlib.pyplot as plt
    
    def canny(image):
        gray  = cv2.cvtColor(lane_image, cv2.COLOR_BGR2GRAY)
        blur  = cv2.GaussianBlur(gray, (5, 5), 0)
        canny = cv2.Canny(blur, 50, 150)
        return canny
    
    def display_lines(image, lines):
        line_image = np.zeros_like(image)
        if lines is not None:
            for line in lines:
                x1, y1, x2, y2 = line.reshape(4)
                cv2.line(line_image, (x1, y1), (x2, y2), (255, 0, 0), 10)
        return line_image
        
        
    def region_of_interest(image):
        height = image.shape[0]
        polygons = np.array([[(200, height), (1100, height), (550, 250)]])
        mask = np.zeros_like(image)
        cv2.fillPoly(mask, polygons, 255)
        masked_image = cv2.bitwise_and(image, mask)
        return masked_image
        
    image = cv2.imread('./images/test_image.jpg')
    lane_image = np.copy(image)
    canny = canny(lane_image)
    cropped_image = region_of_interest(canny)
    lines = cv2.HoughLinesP(cropped_image, 2, np.pi/180, 100, np.array([]), minLineLength=40, maxLineGap=5)
    line_image = display_lines(lane_image, lines)
    combo_image = cv2.addWeighted(lane_image, 0.8, line_image, 1, 1)
    
    cv2.imshow("Region Of Interest", combo_image)
    cv2.waitKey(0)
    ```
    
    * Finally, the detected lines are combined with the original image using `cv2.addWeighted()` and stored in `combo_image`.
        
        ```python
        combo_image = cv2.addWeighted(lane_image, 0.8, line_image, 1, 1)
        ```
        
* **Displaying the Result**:
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714185731542/20014f00-4b0a-4a1c-8d13-fff344c0b260.png align="center")
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714185861717/bc516035-8929-4215-8885-fa17cab70de3.png align="center")

```python
import cv2
import numpy as np

def make_coordinates(image, line_parameters):
    slope, intercept = line_parameters
    y1 = int(image.shape[0])
    y2 = int(y1*3/5)        
    x1 = int((y1 - intercept)/slope)
    x2 = int((y2 - intercept)/slope)
    return [[x1, y1, x2, y2]]

def average_slope_intercept(image, lines):
    left_fit    = []
    right_fit   = []
    if lines is None:
        return None
    for line in lines:
        for x1, y1, x2, y2 in line:
            parameters = np.polyfit((x1,x2), (y1,y2), 1)
            slope = parameters[0]
            intercept = parameters[1]
            if slope < 0: # y is reversed in image
                left_fit.append((slope, intercept))
            else:
                right_fit.append((slope, intercept))
                
    # add more weight to longer lines
    left_fit_average  = np.average(left_fit, axis=0)
    right_fit_average = np.average(right_fit, axis=0)
    left_line  = make_coordinates(image, left_fit_average)
    right_line = make_coordinates(image, right_fit_average)
    averaged_lines = [left_line, right_line]
    return averaged_lines

def canny(image):
    gray = cv2.cvtColor(image, cv2.COLOR_RGB2GRAY)
    blur = cv2.GaussianBlur(gray,(5, 5),0)
    canny = cv2.Canny(gray, 50, 150)
    return canny

def display_lines(image, lines):
    line_image = np.zeros_like(image)
    if lines is not None:
        for line in lines:
            for x1, y1, x2, y2 in line:
                cv2.line(line_image,(x1,y1),(x2,y2),(255,0,0),10)
    return line_image

def region_of_interest(image):
    height = image.shape[0]
    mask = np.zeros_like(image)
    polygons = np.array([[(200, height), (550, 250), (1100, height),]], np.int32)
    cv2.fillPoly(mask, polygons, 255)
    masked_image = cv2.bitwise_and(image, mask)
    return masked_image


image = cv2.imread('./images/test_image.jpg')
lane_image = np.copy(image)
lane_canny = canny(lane_image)
cropped_canny = region_of_interest(lane_canny)
lines = cv2.HoughLinesP(cropped_canny, 2, np.pi/180, 100, np.array([]), minLineLength=40,maxLineGap=5)
averaged_lines = average_slope_intercept(image, lines)
line_image = display_lines(lane_image, averaged_lines)
combo_image = cv2.addWeighted(lane_image, 0.8, line_image, 1, 1)

cv2.imshow("result", combo_image)
cv2.waitKey(0)
```

**Defining Coordinates and Averaging Slope Intercept**:

* The function `make_coordinates()` calculates the coordinates of the lanes based on the line parameters, and it returns a list of line coordinates.
    
* The function `average_slope_intercept()` takes the image and detected lines as input and performs the following operations:
    
    * Iterates through the detected lines and calculates their slopes and intercepts.
        
    * Groups the lines into left and right lanes based on their slopes (negative for the left lane and positive for the right lane).
        
    * Averages the slopes and intercepts of the left and right lanes, giving more weight to longer lines.
        
    * Calculates the coordinates of the averaged left and right lines using the `make_coordinates()` function and returns them as a list of averaged lines.
        

**Canny Edge Detection**: The `canny()` function performs Canny edge detection on the input image using the grayscale conversion, Gaussian blur, and the Canny edge detection algorithm. The resulting edges are returned.

**Displaying Detected Lines**: The `display_lines()` function takes the original image and the detected lines as input, and it draws the detected lines on a blank image.

**Defining the Region of Interest**: The `region_of_interest()` function defines a region of interest using a polygon and creates a mask for the input image. It then isolates the region of interest using the mask and returns the masked image.

**Image Processing for Lane Detection**:

* The code reads an image from the file "test\_image.jpg" and stores it in the variable `image`. A copy of the original image is made and stored in `lane_image`.
    
* Canny edge detection is applied to `lane_image`, and the result is stored in `lane_canny`.
    
* The region of interest is isolated using `region_of_interest()`, and the resulting image is stored in `cropped_canny`.
    
* Hough line transform is applied to the cropped Canny image using `cv2.HoughLinesP()` to detect the lines. The detected lines are then averaged using the `average_slope_intercept()` function.
    
* The function `display_lines()` is used to draw the averaged lines on a blank image, and the result is stored in `line_image`.
    
* The original image and the detected lines are combined using `cv2.addWeighted()` and stored in `combo_image`.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714205570187/e1d0c0a7-5ad6-4bbf-8b51-a2a2293e4a3f.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714205880549/1217577a-d884-4994-802e-c496760eb54b.png align="center")

Now, we applied it all in an image let's apply the same in a video.

```python
import cv2
import numpy as np

def make_points(image, line):
    slope, intercept = line
    y1 = int(image.shape[0])
    y2 = int(y1*3/5)        
    x1 = int((y1 - intercept)/slope)
    x2 = int((y2 - intercept)/slope)
    return [[x1, y1, x2, y2]]

def average_slope_intercept(image, lines):
    left_fit    = []
    right_fit   = []
    if lines is None:
        return None
    for line in lines:
        for x1, y1, x2, y2 in line:
            fit = np.polyfit((x1,x2), (y1,y2), 1)
            slope = fit[0]
            intercept = fit[1]
            if slope < 0: # y is reversed in image
                left_fit.append((slope, intercept))
            else:
                right_fit.append((slope, intercept))
    # add more weight to longer lines
    left_fit_average  = np.average(left_fit, axis=0)
    right_fit_average = np.average(right_fit, axis=0)
    left_line  = make_points(image, left_fit_average)
    right_line = make_points(image, right_fit_average)
    averaged_lines = [left_line, right_line]
    return averaged_lines

def canny(img):
    gray = cv2.cvtColor(img, cv2.COLOR_RGB2GRAY)
    kernel = 5
    blur = cv2.GaussianBlur(gray,(kernel, kernel),0)
    canny = cv2.Canny(gray, 50, 150)
    return canny

def display_lines(img,lines):
    line_image = np.zeros_like(img)
    if lines is not None:
        for line in lines:
            for x1, y1, x2, y2 in line:
                cv2.line(line_image,(x1,y1),(x2,y2),(255,0,0),10)
    return line_image

def region_of_interest(canny):
    height = canny.shape[0]
    width = canny.shape[1]
    mask = np.zeros_like(canny)

    triangle = np.array([[
    (200, height),
    (550, 250),
    (1100, height),]], np.int32)

    cv2.fillPoly(mask, triangle, 255)
    masked_image = cv2.bitwise_and(canny, mask)
    return masked_image

cap = cv2.VideoCapture("./videos/test_video.mp4")
while(cap.isOpened()):
    _, frame = cap.read()
    canny_image = canny(frame)
    cropped_canny = region_of_interest(canny_image)
    lines = cv2.HoughLinesP(cropped_canny, 2, np.pi/180, 100, np.array([]), minLineLength=40,maxLineGap=5)
    averaged_lines = average_slope_intercept(frame, lines)
    line_image = display_lines(frame, averaged_lines)
    combo_image = cv2.addWeighted(frame, 0.8, line_image, 1, 1)
    cv2.imshow("result", combo_image)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
    
cap.release()
cv2.destroyAllWindows()
```

**Defining Helper Functions**:

* The `make_points()` function takes an image and a line's slope and intercept parameters as input. It calculates the coordinates of the endpoints of the line based on the image shape and the line parameters and returns a list of line coordinates.
    
* The `average_slope_intercept()` function takes the image and detected lines as input and performs the following operations:
    
    * Iterates through the detected lines and calculates their slopes and intercepts using linear regression (polyfit).
        
    * Groups the lines into left and right lanes based on their slopes (negative for the left lane and positive for the right lane).
        
    * Averages the slopes and intercepts of the left and right lanes, giving more weight to longer lines, and calculates the coordinates of the averaged left and right lines using the `make_points()` function. It then returns a list of averaged lines.
        
* The `canny()`, the function performs Canny edge detection on the input image using the grayscale conversion, Gaussian blur, and Canny edge detection algorithm. The resulting edges are returned.
    
* The `display_lines()` function takes the original image and the detected lines as input, draws the detected lines on a blank image, and returns the resulting image.
    
* The `region_of_interest()` function defines a region of interest using a polygon, creates a mask for the input image, isolates the region of interest using the mask, and returns the masked image.
    

**Processing Video Frames**:

* The code takes video frames from the file "test\_[video.mp](http://video.mp)4" and processes each frame in a loop.
    
* For each frame, it performs the following operations:
    
    * Applies Canny edge detection to the frame using the `canny()` function.
        
    * Isolates the region of interest within the Canny image using the `region_of_interest()` function.
        
    * Uses the Hough line transform to detect lines in the cropped Canny image.
        
    * Averages and calculates the coordinates of the detected lines using the `average_slope_intercept()` function.
        
    * Draws the averaged lines on a blank image using the `display_lines()` function and combines the original frame with the detected lines using `cv2.addWeighted()`.
        
    * Displays the resulting image with the detected and averaged lines in a window titled "result".
        
* The processing loop continues until the user presses the 'q' key, at which point the video stream is released and all windows are closed using `cap.release()` and `cv2.destroyAllWindows()`.
    

```python
cap = cv2.VideoCapture("./videos/test_video.mp4")
while(cap.isOpened()):
    _, frame = cap.read()
    canny_image = canny(frame)
    cropped_canny = region_of_interest(canny_image)
    lines = cv2.HoughLinesP(cropped_canny, 2, np.pi/180, 100, np.array([]), minLineLength=40,maxLineGap=5)
    averaged_lines = average_slope_intercept(frame, lines)
    line_image = display_lines(frame, averaged_lines)
    combo_image = cv2.addWeighted(frame, 0.8, line_image, 1, 1)
    cv2.imshow("result", combo_image)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
    
cap.release()

# Explaination:
# Open the video file for reading frames
cap = cv2.VideoCapture("./videos/test_video.mp4")

# Continuously process frames from the video
while(cap.isOpened()):
    # Read a frame from the video
    _, frame = cap.read()
    
    # Apply Canny edge detection to the current frame
    canny_image = canny(frame)
    
    # Isolate the region of interest within the Canny edge-detected frame
    cropped_canny = region_of_interest(canny_image)
    
    # Detect lines using Hough line transform
    lines = cv2.HoughLinesP(cropped_canny, 2, np.pi/180, 100, np.array([]), minLineLength=40, maxLineGap=5)
    
    # Average and calculate the coordinates of the detected lines
    averaged_lines = average_slope_intercept(frame, lines)
    
    # Display the detected and averaged lines on the original frame
    line_image = display_lines(frame, averaged_lines)
    
    # Combine the original frame with the detected lines
    combo_image = cv2.addWeighted(frame, 0.8, line_image, 1, 1)
    
    # Display the resulting image with the detected and averaged lines
    cv2.imshow("result", combo_image)
    
    # Check for user input to terminate the video processing
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

# Release the video capture and close all windows
cap.release()
cv2.destroyAllWindows()
```

**Opening a Video File**:

* `cv2.VideoCapture("./videos/test_`[`video.mp`](http://video.mp)`4")`: This line initializes the capture object `cap` to read the video frames from the file "test\_[video.mp](http://video.mp)4" located in the "videos" directory. The file path specifies the location of the video file to be opened.
    
    **Processing Video Frames**:
    
    * `while(cap.isOpened()):`: This starts a while loop that continuously processes frames from the video as long as the video capture `cap` is open.
        
    
    **Frame Processing Steps**:
    
    * `_, frame =`[`cap.read`](http://cap.read)`()`: This line reads a frame from the video capture `cap` and stores it in the variable `frame`. The underscore (`_`) is used to discard the return value indicating whether a new frame was successfully read.
        
    * `canny_image = canny(frame)`: It applies Canny edge detection to the current frame using the `canny()` function, returning the edges detected in the frame.
        
    * `cropped_canny = region_of_interest(canny_image)`: This step isolates the region of interest within the Canny edge-detected frame using the `region_of_interest()` function. The function returns the masked image.
        
    * `lines = cv2.HoughLinesP(cropped_canny, 2, np.pi/180, 100, np.array([]), minLineLength=40, maxLineGap=5)`: Hough line transform is applied to the cropped Canny image to detect the lines. The parameters for the Hough transform are specified (rho, theta, threshold, minLineLength, maxLineGap), and the detected lines are stored in the variable `lines`.
        
    * `averaged_lines = average_slope_intercept(frame, lines)`: The detected lines are then averaged and their coordinates calculated using the `average_slope_intercept()` function. The function returns the averaged lines.
        
    * `line_image = display_lines(frame, averaged_lines)`: The averaged lines are then displayed on a blank image using the `display_lines()` function, and the resulting image with the detected lines is stored in `line_image`.
        
    * `combo_image = cv2.addWeighted(frame, 0.8, line_image, 1, 1)`: The original frame is combined with the detected lines using the `cv2.addWeighted()` function, applying 80% weight to the original frame and 100% weight to the detected lines, and the result is stored in `combo_image`.
        
    * `cv2.imshow("result", combo_image)`: The resulting image with the detected and averaged lines is displayed in a window titled "result" using the `cv2.imshow()` function.
        
    
    **User Interaction and Video Termination**:
    
    * `if cv2.waitKey(1) & 0xFF == ord('q'):`: This line waits for a keyboard event for 1 millisecond and checks if the 'q' key has been pressed. If the 'q' key has been pressed, the code breaks out of the while loop and proceeds to release the video stream.
        
    * `break`: This statement breaks out of the while loop when the 'q' key is pressed.
        
    * `cap.release()`: Finally, the video capture is released using, `cap.release()`, closing the video file and releasing any associated system resources.
        

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1714207813835/14b47e71-76ef-448d-bbb9-836caa76e6e3.gif align="center")

![Best Car Repair & Service Center in Noida](https://apnagarage.in/wp-content/uploads/2022/06/YDLQ.gif align="left")

Thank you for reading this technical blog post.