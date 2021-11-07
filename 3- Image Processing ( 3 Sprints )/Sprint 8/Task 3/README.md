# 1- What ’re the methods that you used ?

<ul>
  <li> Functions used in image processing for <b>OpenCv</b> package: </li>
  <ul>
    <li>cv2.erode(src, kernel[, dst[, anchor[, iterations[, borderType[, borderValue]]]]])</li>
    <li>cv2.threshold(source, thresholdValue, maxVal, thresholdingTechnique)</li>
    <li>cv2.adaptiveThreshold(source, maxVal, adaptiveMethod, thresholdType, blocksize, constant)</li>
    <li>cv2.threshold(source, thresholdValue, maxVal, thresholdingTechnique)</li>
    </ul>
  </ul>

# 2- Explain each method ..


|**Parameters**|            <b>cv2.erode(src, kernel[, dst[, anchor[, iterations[, borderType[, borderValue]]]]])</b>|
|----------|-------------------------------------------------|
|src| It is the image which is to be eroded .|
|kernel| A structuring element used for erosion. If element = Mat(), a 3 x 3 rectangular structuring element is used. Kernel can be created using getStructuringElement.|
|dst| It is the output image of the same size and type as src.|
|anchor| It is a variable of type integer representing anchor point and it’s default value Point is (-1, -1) which means that the anchor is at the kernel center.|
|borderType| It depicts what kind of border to be added. It is defined by flags like cv2.BORDER_CONSTANT, cv2.BORDER_REFLECT, etc.|
|iterations| It is number of times erosion is applied.|
|borderValue| It is border value in case of a constant border.|
|Return Value| It returns an image.|


|**Parameters**|            <b>cv2.threshold(source, thresholdValue, maxVal, thresholdingTechnique)</b>|
|----------|-------------------------------------------------|
|source| Input Image array (must be in Grayscale).|
|thresholdValue| Value of Threshold below and above which pixel values will change accordingly.|
|maxVal| Maximum value that can be assigned to a pixel.|
|thresholdingTechnique| The type of thresholding to be applied.|

 
|**Parameters**|            <b>cv2.adaptiveThreshold(source, maxVal, adaptiveMethod, thresholdType, blocksize, constant)</b>|
|----------|-------------------------------------------------|
|source|  Input Image array(Single-channel, 8-bit or floating-point)|
|maxVal|Maximum value that can be assigned to a pixel.|
|adaptiveMethod| Adaptive method decides how threshold value is calculated.|
|cv2.ADAPTIVE_THRESH_MEAN_C|Threshold Value = (Mean of the neighbourhood area values – constant value). In other words, it is the mean of the blockSize×blockSize neighborhood of a point minus constant.|
|cv2.ADAPTIVE_THRESH_GAUSSIAN_C| Threshold Value = (Gaussian-weighted sum of the neighbourhood values – constant value). In other words, it is a weighted sum of the blockSize×blockSize neighborhood of a point minus constant.|
|thresholdType| The type of thresholding to be applied.|
|blockSize| Size of a pixel neighborhood that is used to calculate a threshold value.|
|constant| A constant value that is subtracted from the mean or weighted sum of the neighbourhood pixels.|


|**Parameters**|            <b>cv2.threshold(source, thresholdValue, maxVal, thresholdingTechnique)</b>|
|----------|-------------------------------------------------|
|source| Input Image array (must be in Grayscale).|
|thresholdValue| Value of Threshold below and above which pixel values will change accordingly.|
|maxVal| Maximum value that can be assigned to a pixel.|
|thresholdingTechnique| The type of thresholding to be applied.|

# 3- What’s new for you ?
> <ul>
> All Of Them is new for me.
> </ul>

# 4- Resources ? 

> [https://www.tutorialspoint.com/opencv/opencv_adaptive_threshold.htm]
>[https://docs.opencv.org/master/d7/d4d/tutorial_py_thresholding.html]

