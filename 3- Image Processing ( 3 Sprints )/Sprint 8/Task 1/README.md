# 1- What ’re the methods that you used ?

<ul>
  <li> Functions used in image processing for <b>OpenCv</b> package: </li>
  <ul>
    <li>cv2.imread(path, flag)</li>
    <li>image.shape</li>
    <li>cv2.imshow(win_name,image)</li>
    <li>cv2.resize(source, dim, fx, fy, interpolation)</li>
    <li>cv2.getRotationMatrix2D((cX, cY), -angle, axis=1.0)</li>
    <li>dst	=	cv.warpAffine(	src, M, dsize[, dst[, flags[, borderMode[, borderValue]]]])</li>
    <li>copy()</li>
    <li>cv2.rectangle(image, starting_coordinate , ending_coordinate, color, thickness, lineType, shift)</li>
    <li>cv2.putText(image, text, org, font, fontScale, color[, thickness[, lineType[, bottomLeftOrigin]]])</li>
    <li>cv2.imshow()</li>
    <li>cv2.getRotationMatrix2D((cX, cY), -angle, axis=1.0)</li>
    <li>cv.warpAffine(	src, M, dsize[, dst[, flags[, borderMode[, borderValue]]]])</li>
    <li>copy()</li>
    <li>cv2.rectangle(image, starting_coordinate , ending_coordinate, color, thickness, lineType, shift)</li>
    <li>cv2.putText(image, text, org, font, fontScale, color, thickness[, lineType[, bottomLeftOrigin]]])</li>
    <li>cv2.waitKey(0)</li>
    <li>cv2.destroyAllWindows()</li>
    <li>cv2.addWeighted(img1, wt1, img2, wt2, gammaValue)</li>
    <li>cv.subtract(src1, src2, dst, mask, dtype)</li>
    <li>cv2.bitwise_and(source1, source2, destination, mask)</li>
    <li>cv2.bitwise_or(source1, source2, destination, mask)</li>
    <li>cv2.bitwise_xor(source1, source2, destination, mask)</li>
    <li>cv2.bitwise_not(source, destination, mask)</li>
    </ul>
  </ul>

# 2- Explain each method ..

|Parameters|            <b>cv2.imread(path, flag) </b>|
|----------|-------------------------------------------------|
|You can pass two parameters to imread() method. Among these two, path parameter is mandatory while flag parameter is optional.|
|**First Parameter**|1. path: location of the image in your system in string form.|
||here two cases can be possible|
||i) if image is present in the current working directory, then you have to mention only the name of the image with their extension like .jpg,.png etc.|
||ii) if image is present at somewhere else in your system not in the current working directory then you have to give complete path, also known as abolute path of the image.|
|**Second Parameter flag:**| This specifies the way in which the image must be read from the system.|
|cv2.IMREAD_UNCHANGED|This flag is used to return the loaded image as is (with alpha channel, otherwise it gets cropped). . Alternatively, we can pass integer value -1 for this flag.|
|cv2.IMREAD_GRAYSCALE|This flag is used to return the image in grayscale format.Alternatively, we can pass integer value 0 for this flag.|
|cv2.IMREAD_COLOR|This flag is used to return the image in BGR color format. It is the **default flag**. Alternatively, we can pass integer value 1 for this flag.|
|cv2.IMREAD_ANYDEPTH|This flag is used to return 16-bit/32-bit image when the input has the corresponding depth, otherwise convert it to 8-bit.Alternatively, we can pass integer value 2 for this flag.|
|cv2.IMREAD_ANYCOLOR|This flag is used to return the image in any possible color format.Alternatively, we can pass integer value 4 for this flag.|
|cv2.IMREAD_LOAD_GDAL|This flag is used the gdal driver for loading the image. Alternatively, we can pass integer value 8 for this flag.|
|cv2.IMREAD_REDUCED_GRAYSCALE_2|This flag is used to return the image in grayscale format and the image size reduced to 1/2 of the original image size .Alternatively, we can pass integer value 16 for this flag.|
|cv2.IMREAD_REDUCED_COLOR_2|This flag is used to return the image in BGR color format and the image size reduced to 1/2 of the original image size.Alternatively, we can pass integer value 17 for this flag.|
|cv2.IMREAD_REDUCED_GRAYSCALE_4|This flag is used to return the image in grayscale format and the image size reduced to 1/4 of the original image size .Alternatively, we can pass integer value 32 for this flag.|
|cv2.IMREAD_REDUCED_COLOR_4|This flag is used to return the image in BGR color format and the image size reduced to 1/4 of the original image size.Alternatively, we can pass integer value 33 for this flag.|
|cv2.IMREAD_REDUCED_GRAYSCALE_8|This flag is used to return the image in grayscale format and the image size reduced to 1/8 of the original image size .Alternatively, we can pass integer value 64 for this flag.|
|cv2.IMREAD_REDUCED_COLOR_8|This flag is used to return the image in BGR color format and the image size reduced to 1/8 of the original image size.Alternatively, we can pass integer value 65 for this flag.|
|**Return value**| This method returns the matrix of pixels which represent the given image. Pixel is nothing but the smallest unit of the image.|


|**image.shape** |returns tuple containing (height, width, number of channels|
|-----------------------------------|-------------------------------------------------|


|**Parameters**|            <b>cv2.imshow(win_name,image) </b>|
|----------|-------------------------------------------------|
|1. **win_name**| Name of the window in which the image will be displayed.|
|2. **image**| Image pixel matrix of that image, which will need to be shown.|
 
|**Parameters**|            <b>cv2.resize(source, dim, fx, fy, interpolation) </b>|
|----------|-------------------------------------------------|
|1. **Source**| Original/Input image i.e that image n-dimensional array which is wanted to be resized.|
|2. **dim**| Required dimension of an image in the form of tuple as (height, width).|
|3. **fx**| Scale factor along the horizontal axis or X- axis.|
|4. **fy**| Scale factor along the vertical axis or Y- axis.|
|5. **interpolation**| This is the process of estimating unknown values that fall between known values. Some methods of interpolation we will mention here which can be used to find-out the pixel value based on its neighboring pixels.|
||INTER_LINEAR: A bilinear interpolation. This is by default method which is used by resize() method.|
||INTER_CUBIC: A bicubic interpolation over 4×4 pixel neighborhood.|
||INTER_LANCZOS4: A Lanczos interpolation over 8×8 pixel neighborhood.|
|**Return Value**|This method returns resized image pixel matrix.|


|Parameters|cv2.getRotationMatrix2D((cX, cY), -angle, axis=1.0)|
|---------------|-------------------------------------------------|
|(cX, cY)|the rotation point|
|angle|Clockwise will be negative and Anticlockwise will positive|
|axis|scale|

|Parameters|dst	=	cv.warpAffine(	src, M, dsize[, dst[, flags[, borderMode[, borderValue]]]])|
|---------------|-------------------------------------------------|
|src|image|
|M|Matrix from the return of cv2.getRotationMatrix2D()|
| dsize[, dst[, flags[, borderMode[, borderValue]]]]|width and height of the image|

|**Parameters**|copy()|
|--------------|------|
|one par|any list|
|return|list|

|**Parameters**|cv2.rectangle(image, starting_coordinate , ending_coordinate, color, thickness, lineType, shift)|
|--------------|------|
|**Mandatory Parameters**|(image,starting_coordinate,ending_coordinate and color)|
|image|Input image of n-dimensional array.|
|starting_coordinate:|Starting top most Left coordinate of the rectangle which is given in the form of tuple.|
|ending_coordinate|Ending bottom most right coordinate of the rectangle which is given in the form of tuple.|
|color| Boundary color of rectangular shape which is given in the form of tuple with respective BGR values.|
|**optional Parameters**|rest(thickness, lineType and shift)|
|thickness| Thickness of rectangle’s boundary (given in pixels). Its default value is 1.|
|lineType| Type of line, whether 8-connected, anti-aliased line etc.By default, it is 8-connected. cv.LINE_AA gives anti-aliased line which looks great for curves.|
|shift| Represents the number of fractional bits in the coordinates.|
|**Return Value**|It returns Output image of n-dimensional array with rectangular shapes drawn on it.|

|**Parameters**|cv2.putText(image, text, org, font, fontScale, color[, thickness[, lineType[, bottomLeftOrigin]]]) |
|--------------|------|
|image| It is the image on which text is to be drawn.|
|text| Text string to be drawn.|
|org| It is the coordinates of the bottom-left corner of the text string in the image. The coordinates are represented as tuples of two values i.e. (X coordinate value, Y coordinate value).|
|font| It denotes the font type. Some of font types are FONT_HERSHEY_SIMPLEX, FONT_HERSHEY_PLAIN, , etc.|
|fontScale| Font scale factor that is multiplied by the font-specific base size.|
|color| It is the color of text string to be drawn. For BGR, we pass a tuple. eg: (255, 0, 0) for blue color.|
|thickness| It is the thickness of the line in px.|
|lineType| This is an optional parameter.It gives the type of the line to be used.|
|bottomLeftOrigin| This is an optional parameter. When it is true, the image data origin is at the bottom-left corner. Otherwise, it is at the top-left corner.|
|**Return Value**| It returns an image.|

|**Parameters**|cv2.waitKey(0)|
|--------------|------|
|one parameter|The time of delay 0 = means forever till the user trigger, delay =1 is 1 ms delay or more|


|**Parameters**|cv2.destroyAllWindows()|
|--------------|------|
|No parameter|simply destroys all the windows we created|

|**Parameters**|cv2.addWeighted(img1, wt1, img2, wt2, gammaValue)|
|--------------|------|
|img1| First Input Image array(Single-channel, 8-bit or floating-point)|
|wt1| Weight of the first input image elements to be applied to the final image|
|img2| Second Input Image array(Single-channel, 8-bit or floating-point)|
|wt2| Weight of the second input image elements to be applied to the final image|
|gammaValue| Measurement of light|
|dst|	output array that has the same size and number of channels as the input arrays.|
|dtype|optional depth of the output array; when both input arrays have the same depth, dtype can be set to -1, which will be equivalent to src1.depth().|


|**Parameters**|cv.subtract(src1, src2, dst, mask, dtype)|
|--------------|------|
|src1|first input array or a scalar.|
|src2|second input array or a scalar.|
|dst|output array of the same size and the same number of channels as the input array.|
|mask|	optional operation mask; this is an 8-bit single channel array that specifies elements of the output array to be changed.|
|dtype|optional depth of the output array|

|**Parameters**|cv2.bitwise_and(source1, source2, destination, mask)|
|--------------|------|
||Bit-wise conjunction of input array elements.|
|source1| First Input Image array(Single-channel, 8-bit or floating-point)|
|source2| Second Input Image array(Single-channel, 8-bit or floating-point)|
|dest| Output array (Similar to the dimensions and type of Input image array)|
|mask| Operation mask, Input / output 8-bit single-channel mask.|


|**Parameters**|cv2.bitwise_or(source1, source2, destination, mask)|
|--------------|------|
||Bit-wise disjunction of input array elements.|
|source1| First Input Image array(Single-channel, 8-bit or floating-point)|
|source2| Second Input Image array(Single-channel, 8-bit or floating-point)|
|dest| Output array (Similar to the dimensions and type of Input image array)|
|mask| Operation mask, Input / output 8-bit single-channel mask.|

|**Parameters**|cv2.bitwise_xor(source1, source2, destination, mask)|
|--------------|------|
||Bit-wise exclusive-OR operation on input array elements.|
|source1| First Input Image array(Single-channel, 8-bit or floating-point)|
|source2| Second Input Image array(Single-channel, 8-bit or floating-point)|
|dest| Output array (Similar to the dimensions and type of Input image array)|
|mask| Operation mask, Input / output 8-bit single-channel mask.|

|**Parameters**|cv2.bitwise_not(source, destination, mask)|
|--------------|------|
|Bitwise NOT operation on Image:|Inversion of input array elements.|
|source1| First Input Image array(Single-channel, 8-bit or floating-point)|
|dest| Output array (Similar to the dimensions and type of Input image array)|
|mask| Operation mask, Input / output 8-bit single-channel mask.|




# 3- What’s new for you ?
> <ul>
> All Of Them is new for me.
> </ul>

# 4- Resources ? 

> [https://java2blog.com/cv2-imread-python/]
> [https://www.geeksforgeeks.org/python-opencv-cv2-puttext-method/]
> [https://docs.opencv.org/master/d2/de8/group__core__array.html#gafafb2513349db3bcff51f54ee5592a19]
> [https://www.pyimagesearch.com/?s=cv2.putText%28%29]
> [https://www.python-course.eu/matplotlib_subplots.php]
> [https://www.tutorialkart.com/opencv/python/opencv-python-resize-image/]
