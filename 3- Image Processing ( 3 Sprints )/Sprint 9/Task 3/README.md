# 1- What ’re the methods that you used ?

<ul>
  <li> Functions used in image processing for <b>OpenCv</b> package: </li>
  <ul>
    <li>cv2.goodFeaturesToTrack()</li>
    <li>numpy.ravel(x, order='C')</li>
    <li>cv2.circle(img, center, radius, color, thickness=1, lineType=8, shift=0)</li>
    <li>inRange(src, lowerb, upperb, dst)</li>
    <li>cv2.cornerHarris(src, dest, blockSize, kSize, freeParameter, borderType)</li>
    <li>cv2.dilate(img,kernel,iterations = 1)</li>
    </ul>
  </ul>

# 2- Explain each method ..

|**Parameters**|<b> cv2.goodFeaturesToTrack(image, maxCorners, qualityLevel,minDistance[, corners[, mask[, blockSize[, useHarrisDetector[, k]]]]]) </b>|
|----------|-------------------------------------------------|
|matrix| The image|
| maxCorners |Feature Detect Max Corners|
|qualityLevel|Feature Detect Quality Level|
|minDistance| Feature Detect Minimum Distance)|

|**Parameters**|<b>numpy.ravel(x, order='C')</b>|
|----------|-------------------------------------------------|
| x| array_like|
|This parameter defines the input array, which we want to change in a contiguous flattened array. The array elements are read in the order specified by the order parameter and packed as a 1-D array.|
|order: {'C','F', 'A', 'K'}(optional)| If we set the order parameter to 'C', it means that the array gets flattened in row-major order. If 'F' is set, the array gets flattened in column-major order. The array is flattened in column-major order only when 'A' is Fortran contiguous in memory, and when we set the order parameter to 'A'. The last order is 'K', which flatten the array in same order in which the elements occurred in the memory. By default, this parameter is set to 'C'.|
|Returns|This function returns a contiguous flatten array with the same data type as an input array and has shape equal to (x.size).|

|**Parameters**|<b>cv2.circle(img, center, radius, color, thickness=1, lineType=8, shift=0)</b>|
|----------|-------------------------------------------------|
|image| It is the image on which circle is to be drawn. |
|center_coordinates| It is the center coordinates of circle. The coordinates are represented as tuples of two values i.e. (X coordinate value, Y coordinate value). |
|radius| It is the radius of circle. 
|color| It is the color of border line of circle to be drawn. For BGR, we pass a tuple. eg: (255, 0, 0) for blue color. 
|thickness| It is the thickness of the circle border line in px. Thickness of -1 px will fill the circle shape by the specified color.
|lineType (int) | Type of the circle boundary, see Line description
|shift (int) | Number of fractional bits in the center coordinates and radius value
|Return Value| It returns an image. 

|**Parameters**|<b> inRange(src, lowerb, upperb, dst) </b>|
|----------|-------------------------------------------------|
|src| The image|
||The lowerb and upperb parameters specify the required lower and upper color bounds in the HSV format. In OpenCV, for HSV, Hue range is [0,179], Saturation range is [0,255] and Value range is [0,255].|
||Start from a color to track in RGB format.|
||Convert the color to the HSV format. Let (H, S, V) be its value.|
||Assign the value (H - deltaH, minS, minV) to lowerb and the value (H - deltaH, maxS, maxV) to upperb.|

|**Parameters**|<b>cv2.cornerHarris(src, dest, blockSize, kSize, freeParameter, borderType)</b>|
|----------|-------------------------------------------------|
|src |Input Image (Single-channel, 8-bit or floating-point)|
|dest | Image to store the Harris detector responses. Size is same as source image|
|blockSize | Neighborhood size ( for each pixel value blockSize * blockSize neighbourhood is considered )|
|ksize | Aperture parameter for the Sobel() operator|
|freeParameter | Harris detector free parameter|
|borderType | Pixel extrapolation method ( the extrapolation mode used returns the coordinate of the pixel corresponding to the specified extrapolated pixel )|

cv2.dilate(img,kernel,iterations = 1)  To increase the Forground

# 3- What’s new for you ?
> <ul>
> All Of Them is new for me.
> </ul>

# 4- Resources ? 

> [https://docs.opencv.org/master/d4/d8c/tutorial_py_shi_tomasi.html]
> [https://www.programcreek.com/python/example/89311/cv2.goodFeaturesToTrack]
> [https://numpy.org/doc/stable/reference/generated/numpy.ravel.html]
> [https://www.javatpoint.com/numpy-ravel]

