# 1- What ’re the methods that you used ?

<ul>
  <li> Functions used in image processing for <b>OpenCv</b> package: </li>
  <ul>
    <li>cv2.canny(image, lower, upper)</li>
    <li>dst = cv.GaussianBlur(src, ksize, sigmaX[, dst[, sigmaY[, borderType=BORDER_DEFAULT]]] )</li>
    <li>medianBlur(src, dst, ksize)</li>
    <li>void bilateralFilter(InputArray src, OutputArray dst, int d, double sigmaColor, double sigmaSpace, int borderType=BORDER_DEFAULT )</li>
    </ul>
  </ul>

# 2- Explain each method ..


|**Parameters**|            <b>cv2.canny(image, lower, upper)</b>|
|----------|-------------------------------------------------|
|1. **Source**| Original/Input image i.e that image n-dimensional array which is wanted to be resized.|
|2.lower|The Lower thresholds|
|3. upper|The Maximum thresholds|

Convolution kernel matrix to detect the pixel in new pic

gaussian : calculate gaussian waighted value - linear operation - does not reserve edges - scanning id or documents - cannot detect the pixels on the high intensity , he works with neghiborhood pixels , new value created using equation 

Median: non linear op - preserving to edges > edge detiction . Convolution kernel matrix by taking median value by neighborhood. used to clear nois . papper and salt noise

Piletiral: time consuming > very slow, edge preserving high quality, non linear using the same  gaussian filter, intensity concept so he can detect edges
	
|**Parameters**|            <b>dst = cv.GaussianBlur(src, ksize, sigmaX[, dst[, sigmaY[, borderType=BORDER_DEFAULT]]] )</b>|
|----------|-------------------------------------------------|
|1. **src**| Original/Input image i.e that image n-dimensional array which is wanted to be resized.|
|2.dst|Output image i.e that image n-dimensional array|
|3. ksize|Gaussian Kernel Size. [height width]. height and width should be odd and can have different values. If ksize is set to [0 0], then ksize is computed from sigma values.|
|sigmaX|Kernel standard deviation along X-axis (horizontal direction).|
|sigmaY|Kernel standard deviation along Y-axis (vertical direction). If sigmaY=0, then sigmaX value is taken for sigmaY|
|borderType|Specifies image boundaries while kernel is applied on image borders. Possible values are : cv.BORDER_CONSTANT cv.BORDER_REPLICATE cv.BORDER_REFLECT cv.BORDER_WRAP cv.BORDER_REFLECT_101 cv.BORDER_TRANSPARENT cv.BORDER_REFLECT101 cv.BORDER_DEFAULT cv.BORDER_ISOLATED|


|**Parameters**|            <b>medianBlur(src, dst, ksize)</b>|
|----------|-------------------------------------------------|
|1. **src**| A Mat object representing the source (input image) for this operation.|
|2.dst| A Mat object representing the destination (output image) for this operation.|
|3. ksize|A Size object representing the size of the kernel.|

|**Parameters**|            <b>void bilateralFilter(InputArray src, OutputArray dst, int d, double sigmaColor, double sigmaSpace, int borderType=BORDER_DEFAULT )</b>|
|----------|-------------------------------------------------|
|1. **src**|Source 8-bit or floating-point, 1-channel or 3-channel image.|
|2. dst| Destination image of the same size and type as src .|
|3. d |Diameter of each pixel neighborhood that is used during filtering. If it is non-positive, it is computed from sigmaSpace .|
|4. sigmaColor | Filter sigma in the color space. A larger value of the parameter means that farther colors within the pixel neighborhood (see sigmaSpace ) will be mixed together, resulting in larger areas of semi-equal color.|
|5. sigmaSpace | Filter sigma in the coordinate space. A larger value of the parameter means that farther pixels will influence each other as long as their colors are close enough (see sigmaColor ). When d>0 , it specifies the neighborhood size regardless of sigmaSpace . Otherwise, d is proportional to sigmaSpace .

# 3- What’s new for you ?
> <ul>
> All Of Them is new for me.
> </ul>

# 4- Resources ? 

> [https://stackoverflow.com/questions/3584805/in-matplotlib-what-does-the-argument-mean-in-fig-add-subplot111]
> [https://docs.opencv.org/master/d4/d13/tutorial_py_filtering.html]
> [https://docs.opencv.org/master/d4/d86/group__imgproc__filter.html]
> [https://www.quora.com/What-are-the-advantages-of-Gaussian-blur-median-blur-and-the-bilateral-filter/answers/21700230?ch=3&share=ab3f6889&srid=3ys1e]
> [https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_imgproc/py_filtering/py_filtering.html]
> [https://stackoverflow.com/questions/4195453/how-to-resize-an-image-with-opencv2-0-and-python2-6]
> [https://www.tutorialkart.com/opencv/python/opencv-python-resize-image/]
> [http://opencvexamples.blogspot.com/2013/10/applying-bilateral-filter.html]
> [https://en.wikipedia.org/wiki/Canny_edge_detector]
> [https://www.tutorialspoint.com/opencv/opencv_median_blur.htm]

