# 1- What ’re the methods that you used ?

<ul>
  <li> Functions used in image processing for <b>OpenCv</b> package: </li>
  <ul>
    <li>cv2.cvtColor(frame, cv2.COLOR_BGR2HSV)</li>
    <li>cv2.Sobel(original_image,ddepth,xorder,yorder,kernelsize)</li>
    <li>cv2.inRange(hsv, lower_red, upper_red)</li>
    <li>cv2.HoughLines(dst, lines, 1, CV_PI/180, 150, 0, 0 )</li>
    </ul>
  </ul>

# 2- Explain each method ..

|**Parameters**|<b>cv2.Sobel(original_image,ddepth,xorder,yorder,kernelsize)</b>|
|----------|-------------------------------------------------|
|first parameter | original image|
|second parameter | the depth of the destination image. ddepth=-1/CV_64F the destination image will have the same depth as the source.|
|third parameter | the order of the derivative x. While we calculate Sobelx we will set xorder as 1 |
|fourth parameter | the order of the derivative y.While we calculate Sobelx we will set yorder as 0 |
|The last parameter | the size of the extended Sobel kernel; it must be 1, 3, 5, or 7.|

|**Parameters**|<b>cv2.Laplacian(frame,cv2.CV_64F)</b>|
|----------|-------------------------------------------------|
|the first parameter | the original image|
|the second parameter| the depth of the destination image.When depth=-1/CV_64F, the destination image will have the same depth as the source.|

|**hreshold HSV image**| cv2.inRange(hsv, lower_red, upper_red)|
|----------|-------------------------------------------------|
|src | the input image.|
|‘lowerb’ and ‘upperb’| denotes the lower and upper boundary of the threshold region. A pixel is set to 255 if it lies within the boundaries specified otherwise set to 0. This way it returns the thresholded image.|

|**Parameters**|cv2.HoughLines(dst, lines, 1, CV_PI/180, 150, 0, 0 )|
|----------|-------------------------------------------------|
|dst| Output of the edge detector. It should be a grayscale image (although in fact it is a binary one)|
|lines|A vector that will store the parameters (r,θ) of the detected lines|
|rho | The resolution of the parameter r in pixels. We use 1 pixel. The distance resolution of accumulator in pixels|
|theta| The resolution of the parameter θ in radians. We use 1 degree (CV_PI/180) The angle resolution of accumulator in pixels|
|threshold| The minimum number of intersections to "*detect*" a line|
|srn and stn| Default parameters to zero. Check OpenCV reference for more info. Accumulator Threshold parameter so the values which returned will be above this value of the threshold|

# 3- What’s new for you ?
> <ul>
> All Of Them is new for me.
> </ul>

# 4- Resources ? 

> [https://www.lifewire.com/what-is-hsv-in-design-1078068]
> [https://www.sciencedirect.com/topics/computer-science/sobel-filter]

