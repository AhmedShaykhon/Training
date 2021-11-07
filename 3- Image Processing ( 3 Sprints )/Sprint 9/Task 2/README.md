# 1- What ’re the methods that you used ?

<ul>
  <li> Functions used in image processing for <b>OpenCv</b> package: </li>
  <ul>
    <li>cv2.matchTemplate(img_gray,template,cv2.TM_CCOEFF_NORMED) </li>
    <li>ORB_create(	[, nfeatures[, scaleFactor[, nlevels[, edgeThreshold[, firstLevel[, WTA_K[, scoreType[, patchSize[, fastThreshold]]]]]]]]]	)</li>
    <li>cv2.BFMatcher()</li>
    <li>drawMatches(img1, keypoints1, img2, keypoints2, matches1to2, outImg[, matchColor[, singlePointColor[, matchesMask[, flags]]]])</li>
    <li>cv.HoughCircles (image, circles, method, dp, minDist, param1 = 100, param2 = 100, minRadius = 0, maxRadius = 0)</li>
    </ul>
  </ul>

# 2- Explain each method ..

|**Parameters**|<b> cv2.matchTemplate(img_gray,template,cv2.TM_CCOEFF_NORMED) </b>|
|----------|-------------------------------------------------|
|First Par|Gray Image Source|
|second Par| is the template to be matched|
|third parameter is the method used for matching.|cv2.TM_CCOEFF|
||cv2.TM_CCOEFF_NORMED|
||cv2.TM_CCORR|
||cv2.TM_CCORR_NORMED|
||cv2.TM_SQDIFF|
||cv2.TM_SQDIFF_NORMED|

|**Parameters**|<b>ORB_create(	[, nfeatures[, scaleFactor[, nlevels[, edgeThreshold[, firstLevel[, WTA_K[, scoreType[, patchSize[, fastThreshold]]]]]]]]]	)</b>|
|----------|-------------------------------------------------|
|nfeatures|	The maximum number of features to retain.|
|scaleFactor|	Pyramid decimation ratio, greater than 1. scaleFactor==2 means the classical pyramid, where each next level has 4x less pixels than the previous, but such a big scale factor will degrade feature matching scores dramatically. On the other hand, too close to 1 scale factor will mean that to cover certain scale range you will need more pyramid levels and so the speed will suffer.|
|nlevels|	The number of pyramid levels. The smallest level will have linear size equal to input_image_linear_size/pow(scaleFactor, nlevels - firstLevel).|
|edgeThreshold	|This is size of the border where the features are not detected. It should roughly match the patchSize parameter.|
|firstLevel|	The level of pyramid to put source image to. Previous layers are filled with upscaled source image.|
|WTA_K	|The number of points that produce each element of the oriented BRIEF descriptor. The default value 2 means the BRIEF where we take a random point pair and compare their brightnesses, so we get 0/1 response. Other possible values are 3 and 4. For example, 3 means that we take 3 random points (of course, those point coordinates are random, but they are generated from the pre-defined seed, so each element of BRIEF descriptor is computed deterministically from the pixel rectangle), find point of maximum brightness and output index of the winner (0, 1 or 2). Such output will occupy 2 bits, and therefore it will need a special variant of Hamming distance, denoted as NORM_HAMMING2 (2 bits per bin). When WTA_K=4, we take 4 random points to compute each bin (that will also occupy 2 bits with possible values 0, 1, 2 or 3).|
|scoreType	|The default HARRIS_SCORE means that Harris algorithm is used to rank features (the score is written to KeyPoint::score and is used to retain best nfeatures features); FAST_SCORE is alternative value of the parameter that produces slightly less stable keypoints, but it is a little faster to compute.|
|patchSize|	size of the patch used by the oriented BRIEF descriptor. Of course, on smaller pyramid layers the perceived image area covered by a feature will be larger.|
|fastThreshold	||

|**Parameters**|<b>cv2.BFMatcher() </b>|
|----------|-------------------------------------------------|
|if emptyTrainData is false| the method creates a deep copy of the object, that is, copies both parameters and train data. If emptyTrainData is true, the method creates an object copy with the current parameters but with empty train data|
|normType	One of NORM_L1, NORM_L2, NORM_HAMMING, NORM_HAMMING2.| L1 and L2 norms are preferable choices for SIFT and SURF descriptors, NORM_HAMMING should be used with ORB, BRISK and BRIEF, NORM_HAMMING2 should be used with ORB when WTA_K==3 or 4 (see ORB::ORB constructor description).|
|crossCheck|	If it is false, this is will be default BFMatcher behaviour when it finds the k nearest neighbors for each query descriptor. If crossCheck==true, then the knnMatch() method with k=1 will only return pairs (i,j) such that for i-th query descriptor the j-th descriptor in the matcher's collection is the nearest and vice versa, i.e. the BFMatcher will only return consistent pairs. Such technique usually produces best results with minimal number of outliers when there are enough matches. This is alternative to the ratio test, used by D. Lowe in SIFT paper.|

|**Parameters**|<b>drawMatches(img1, keypoints1, img2, keypoints2, matches1to2, outImg[, matchColor[, singlePointColor[, matchesMask[, flags]]]]) -> outImg @brief Draws the found matches of keypoints from two images.</b>|
|----------|-------------------------------------------------|
|img1 |First source image.|
| keypoints1| Keypoints from the first source image.|
| img2| Second source image.|
| keypoints2 |Keypoints from the second source image.|
| matches1to2| Matches from the first image to the second one, which means that keypoints1[i]|
|has a corresponding point| in keypoints2[matches[i]] .|
| outImg Output image| Its content depends on the flags value defining what is drawn in the output image. See possible flags bit values below.|
|| @param matchColor Color of matches (lines and connected keypoints). If matchColor==Scalar::all(-1)|
||, the color is generated randomly.|
|| @param singlePointColor Color of single keypoints (circles), which means that keypoints do not have the matches. If singlePointColor==Scalar::all(-1) , the color is generated randomly.|
||@param matchesMask Mask determining which matches are drawn. If the mask is empty, all matches are drawn.|
||@param flags Flags setting drawing features. Possible flags bit values are defined by DrawMatchesFlags.|
|| This function draws matches of keypoints from two images in the output image. Match is a line connecting two keypoints (circles). See cv::DrawMatchesFlags.|



|**Parameters**|<b>cv.HoughCircles (image, circles, method, dp, minDist, param1 = 100, param2 = 100, minRadius = 0, maxRadius = 0)</b>|
|----------|-------------------------------------------------|
|image|	8-bit, single-channel, grayscale input image.|
|circles|	output vector of found circles(cv.CV_32FC3 type). Each vector is encoded as a 3-element floating-point vector (x,y,radius) .|
|method	detection| method(see cv.HoughModes). Currently, the only implemented method is HOUGH_GRADIENT|
|dp	|inverse ratio of the accumulator resolution to the image resolution. For example, if dp = 1 , the accumulator has the same resolution as the input image. If dp = 2 , the accumulator has half as big width and height.|
|minDist	|minimum distance between the centers of the detected circles. If the parameter is too small, multiple neighbor circles may be falsely detected in addition to a true one. If it is too large, some circles may be missed.|
|param1|	first method-specific parameter. In case of HOUGH_GRADIENT , it is the higher threshold of the two passed to the Canny edge detector (the lower one is twice smaller).|
|param2|	second method-specific parameter. In case of HOUGH_GRADIENT , it is the accumulator threshold for the circle centers at the detection stage. The smaller it is, the more false circles may be detected. Circles, corresponding to the larger accumulator values, will be returned first.|
|minRadius|	minimum circle radius.|
|maxRadius|	maximum circle radius.|

# 3- What’s new for you ?
> <ul>
> All Of Them is new for me.
> </ul>

# Resources

[https://docs.opencv.org/2.4/doc/tutorials/imgproc/histograms/template_matching/template_matching.html]
[https://github.com/methylDragon/opencv-python-reference/blob/master/02%20OpenCV%20Feature%20Detection%20and%20Description.md]
[https://www.sicara.ai/blog/object-detection-template-matching?fbclid=IwAR0M6t4NI4iZlbP2usWf-d1brwm7SeTtHP4o5csBVIfJxKTollesXSu9wIw]
[https://www.pyimagesearch.com/2015/01/26/multi-scale-template-matching-using-python-opencv/?fbclid=IwAR3PPHv7RV11GEj8h17u7qNJXGQQ8Q7POuOHw-5s3zE2oHLBgG9JNCynUok]
[https://docs.opencv.org/3.4/d3/de5/tutorial_js_houghcircles.html]

