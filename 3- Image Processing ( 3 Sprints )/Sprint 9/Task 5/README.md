1- What ’re the methods that you used ?
<ul>
  <li> Functions used in image processing for <b>OpenCv</b> package: </li>
  <ul>
    <li>cv2.detectMultiScale(	image[, scaleFactor[, minNeighbors[, flags[, minSize[, maxSize]]]]]	)</li>
    </ul>
  </ul>



2- Explain each method ..

|**Parameters**|<b> cv2.detectMultiScale(	image[, scaleFactor[, minNeighbors[, flags[, minSize[, maxSize]]]]]	) </b>|
|----------|-------------------------------------------------|
|image|	Matrix of the type CV_8U containing an image where objects are detected.|
|objects	|Vector of rectangles where each rectangle contains the detected object, the rectangles may be partially outside the original image.|
|scaleFactor|	Parameter specifying how much the image size is reduced at each image scale.|
|minNeighbors|	Parameter specifying how many neighbors each candidate rectangle should have to retain it.|
|flags|	Parameter with the same meaning for an old cascade as in the function cvHaarDetectObjects. It is not used for a new cascade.|
|minSize|	Minimum possible object size. Objects smaller than that are ignored.|
|maxSize|	Maximum possible object size. Objects larger than that are ignored. If maxSize == minSize model is evaluated on single scale.|


3- Resources ? 

> [https://towardsdatascience.com/a-guide-to-face-detection-in-python-3eab0f6b9fc1]
> [https://www.bogotobogo.com/python/OpenCV_Python/python_opencv3_Image_Object_Detection_Face_Detection_Haar_Cascade_Classifiers.php]
