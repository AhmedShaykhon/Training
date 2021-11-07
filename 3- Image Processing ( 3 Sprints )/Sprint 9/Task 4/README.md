# 1- What ’re the methods that you used ?

<ul>
  <li> Functions used in image processing for <b>OpenCv</b> package: </li>
  <ul>
    <li>cv2.calcOpticalFlowPyrLK(prevImg, nextImg, prevPts, nextPts[, winSize[, maxLevel[, criteria]]])</li>
    <li>numpy.zeros_like(array, dtype = None, order = ‘K’, subok = True)</li>
    <li>cv.normalize(src, dst, alpha = 1, beta = 0, norm_type = NORM_L2, dtype = -1,, mask = Cv::Mat.new())</li>
    <li>cv2.threshold(source, thresholdValue, maxVal, thresholdingTechnique)</li>
    </ul>
  </ul>

# 2- Explain each method ..

|**Parameters**|<b> Syntax: cv2.calcOpticalFlowPyrLK(prevImg, nextImg, prevPts, nextPts[, winSize[, maxLevel[, criteria]]]) </b>|
|----------|-------------------------------------------------|
|1. prevImg |first 8-bit input image|
|2. nextImg | second input image|
|3. prevPts | vector of 2D points for which the flow needs to be found.|
|4. winSize | size of the search window at each pyramid level.|
|5. maxLevel | 0-based maximal pyramid level number; if set to 0, pyramids are not used (single level), if set to 1, two levels are used, and so on.|
|6. criteria | parameter, specifying the termination criteria of the iterative search algorithm.|
|Return|**-nextPts** – output vector of 2D points (with single-precision floating-point coordinates) containing the calculated new positions of input features in the second image; when OPTFLOW_USE_INITIAL_FLOW flag is passed, the vector must have the same size as in the input.|
||**- status** – output status vector (of unsigned chars); each element of the vector is set to 1 if the flow for the corresponding features has been found, otherwise, it is set to 0.|
||**- err** – output vector of errors; each element of the vector is set to an error for the corresponding feature, type of the error measure can be set in flags parameter; if the flow wasn’t found then the error is not defined (use the status parameter to find such cases).|

np.random.randint(start, stop, size of array(x, y)) 


|**Parameters**|<b> Syntax:numpy.zeros_like(array, dtype = None, order = ‘K’, subok = True) : </b>|
|----------|-------------------------------------------------|
|array | array_like input|
|subok | [optional, boolean]If true, then newly created array will be sub-class of array; otherwise, a base-class array|
|order | C_contiguous or F_contiguous|
||  C-contiguous order in memory(last index varies the fastest)|
||  C order means that operating row-rise on the array will be slightly quicker|
||  FORTRAN-contiguous order in memory (first index varies the fastest).|
||  F order means that column-wise operations will be faster. |
|dtype  | [optional, float(byDeafult)] Data type of returned array.|
|Return |array of given shape and type as given array, with zeros - ndarray of zeros having given shape, order and datatype|


|**Parameters**|<b>cv.normalize(src, dst, alpha = 1, beta = 0, norm_type = NORM_L2, dtype = -1,, mask = Cv::Mat.new()) ⇒ Void</b>|
|----------|-------------------------------------------------|
|src | (Cv::Mat)|
|dst| (Cv::Mat)|
|alpha| (Double) (defaults to: 1)|
|beta| (Double) (defaults to: 0)|
|norm_type| (Fixnum) (defaults to: NORM_L2)|
|dtype| (Fixnum) (defaults to: -1,)|
|mask| (Cv::Mat) (defaults to: Cv::Mat.new())|
|Returns:|(Void)|

|**Parameters**|<b>cv2.threshold(source, thresholdValue, maxVal, thresholdingTechnique)</b>|
|----------|-------------------------------------------------|
||(T, threshImage) = cv2.threshold(src, thresh, maxval, type)|
|source| Input Image array (must be in Grayscale).|
| thresholdValue| Value of Threshold below and above which pixel values will change accordingly.|
| maxVal| Maximum value that can be assigned to a pixel.|
| thresholdingTechnique| The type of thresholding to be applied.|
|The different Simple Thresholding Techniques are:||
|cv2.THRESH_BINARY| If pixel intensity is greater than the set threshold, value set to 255, else set to 0 (black).|
|cv2.THRESH_BINARY_INV| Inverted or Opposite case of cv2.THRESH_BINARY.|
|cv.THRESH_TRUNC| If pixel intensity value is greater than threshold, it is truncated to the threshold. The pixel values are set to be the same as the threshold. All other values remain the same.|
|cv.THRESH_TOZERO| Pixel intensity is set to 0, for all the pixels intensity, less than the threshold value.|
|cv.THRESH_TOZERO_INV| Inverted or Opposite case of cv2.THRESH_TOZERO.|


|**Parameters**|<b>cv2.findContours(src, contour_retrieval, contours_approximation)</b>|
|----------|-------------------------------------------------|
|src| Input Image of n – dimensional array(n = 2,3) but preferred 2-dim binary images for better result.|
|contour_retrieval| This is contour retrieval mode. Possible values are |
||a) cv2.RETR_TREE|
||b) cv2.RETR_EXTERNAL|
||c) cv2.RETR_LIST|
||d) cv2.RETR_CCOMP etc.|
|contours_approximation: This is Contour approximation method. Possible values are :||
||a) cv2.CHAIN_APPROX_NONE|
||b) cv2.CHAIN_APPROX_SIMPLE|
||Return Value|It returns three values :|
||a) Input image array|
||b) Contours|
||c) Hierarchy|


contours, hierarchy = cv2.findContours(edged, cv2.RETR_EXTERNAL, cv2.CHAIN_APPROX_NONE)  
cv2.drawContours(image, contours, -1, (0, 255, 0), 3)) [-1 signifies drawing all contours ]


|**Parameters**|<b>cv2.rectangle(image, start_point, end_point, color, thickness)</b>|
|----------|-------------------------------------------------|
|image| It is the image on which rectangle is to be drawn.|
|start_point| It is the starting coordinates of rectangle. The coordinates are represented as tuples of two values i.e. (X coordinate value, Y coordinate value).|
|end_point| It is the ending coordinates of rectangle. The coordinates are represented as tuples of two values i.e. (X coordinate value, Y coordinate value).|
|color| It is the color of border line of rectangle to be drawn. For BGR, we pass a tuple. eg: (255, 0, 0) for blue color.|
|thickness| It is the thickness of the rectangle border line in px. Thickness of -1 px will fill the rectangle shape by the specified color.|



|**Parameters**|<b>cv2.putText(image, text, org, font, fontScale, color[, thickness[, lineType[, bottomLeftOrigin]]])</b>|
|----------|-------------------------------------------------|
|image| It is the image on which text is to be drawn.|
|text| Text string to be drawn.|
|org| It is the coordinates of the bottom-left corner of the text string in the image. The coordinates are represented as tuples of two values i.e. (X coordinate value, Y coordinate value).|
|font| It denotes the font type. Some of font types are FONT_HERSHEY_SIMPLEX, FONT_HERSHEY_PLAIN, , etc.|
|fontScale| Font scale factor that is multiplied by the font-specific base size.|
|color| It is the color of text string to be drawn. For BGR, we pass a tuple. eg: (255, 0, 0) for blue color.|
|thickness| It is the thickness of the line in px.|
|lineType| This is an optional parameter.It gives the type of the line to be used.|
|bottomLeftOrigin| This is an optional parameter. When it is true, the image data origin is at the bottom-left corner. Otherwise, it is at the top-left corner.|
|Return Value| It returns an image.|

|**Parameters**|<b>cv2.putText(image, text, org, font, fontScale, color[, thickness[, lineType[, bottomLeftOrigin]]] method is used to draw a text string on any image.)</b>|
|----------|-------------------------------------------------|
|image| It is the image on which text is to be drawn.|
|text| Text string to be drawn.|
|org| It is the coordinates of the bottom-left corner of the text string in the image. The coordinates are represented as tuples of two values i.e. (X coordinate value, Y coordinate value).|
|font| It denotes the font type. Some of font types are FONT_HERSHEY_SIMPLEX, FONT_HERSHEY_PLAIN, , etc.|
|fontScale| Font scale factor that is multiplied by the font-specific base size.|
|color| It is the color of text string to be drawn. For BGR, we pass a tuple. eg: (255, 0, 0) for blue color.|
|thickness| It is the thickness of the line in px.|
|lineType| This is an optional parameter.It gives the type of the line to be used.|
|bottomLeftOrigin| This is an optional parameter. When it is true, the image data origin is at the bottom-left corner. Otherwise, it is at the top-left corner.|
|Return Value| It returns an image.|
# 3- What’s new for you ?
> <ul>
> All Of Them is new for me.
> </ul>

# 4- Resources ? 

> [https://www.geeksforgeeks.org/python-opencv-optical-flow-with-lucas-kanade-method/?ref=lbp]
> [https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_video/py_lucas_kanade/py_lucas_kanade.html]
> [https://www.programcreek.com/python/example/89363/cv2.calcOpticalFlowPyrLK]
> [https://www.rubydoc.info/gems/ropencv/0.0.21/OpenCV%2FCv.normalize]
> [https://www.pyimagesearch.com/2014/09/08/thresholding-simple-image-segmentation-using-opencv/]
> [https://docs.opencv.org/master/d7/d4d/tutorial_py_thresholding.html]
