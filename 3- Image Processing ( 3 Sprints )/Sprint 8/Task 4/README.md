# 1- What ’re the methods that you used ?

<ul>
  <li> Functions used in image processing for <b>OpenCv</b> package: </li>
  <ul>
    <li>cv2.VideoCapture</li>
    <li>read()</li>
    <li>cv2.imwrite()</li>
    <li>cv2.CascadeClassifier.detectMultiScale(image, scaleFactor, minNeighbors, flags, minSize, maxSize)</li>
    <li>cap.isOpened()</li>
    <li>cv2.cvtColor(im, cv2.COLOR_BGR2GRAY)</li>
    <li>face_cascade.detectMultiScale(gray, 1.3, 4)</li>
    <li>cv2.rectangle(img, (x, y), (x + w, y + h), (255, 0, 0), 4)</li>
    <li>os.path.join(datasets, subdir)</li>
    <li>cv2.face.LBPHFaceRecognizer_create()</li>
    <li>cv2.putText(im, '% s - %.0f' %(names[prediction[0]], prediction[1]), (x-10, y-10),cv2.FONT_HERSHEY_PLAIN, 1, (0, 255, 0))</li>
    </ul>
  </ul>

# 2- Explain each method ..

|**Parameters**|<b>cv2.VideoCapture(video_path or device index ) </b>|
|----------|-------------------------------------------------|
|video_path| Locationvideo in your system in string form with their extensions like .mp4, .avi, etc.|
|device index|It is just the number to specify the camera. Its possible values ie either 0 or -1.|
|or image sequence (eg. img_%02d.jpg, which will read samples like img_00.jpg, img_01.jpg, img_02.jpg, ...)|
|or URL of video stream| (eg. protocol://host:port/script_name?script_paramsauth)|
|or GStreamer| pipeline string in gst-launch tool format in case if GStreamer is used as backend Note that each video stream or IP camera feed has its own URL scheme. Please refer to the documentation of source stream to know the right URL.|
|Return value|Video capture object.|

cap.isOpened() : Returns true if video capturing has been initialized already.


|**Parameters**|<b>read() </b>|
|----------|-------------------------------------------------|
|filename| A string representing the file name. The filename must include image format like .jpg, .png, etc.|
|Return Value 1| returns True if the video still running|
|return Value 2| 1- OpenCV 1.x functions cvRetrieveFrame and cv.RetrieveFrame return image stored inside the video capturing structure. It is not allowed to modify or release the image! You can copy the frame using :ocvcvCloneImage and then do whatever you want with the copy.


|**Parameters**|<b>cv2.imwrite() </b>|
|----------|-------------------------------------------------|
|filename| A string representing the file name. The filename must include image format like .jpg, .png, etc.|
|image| It is the image that is to be saved.|
|Return Value| It returns true if image is saved successfully.|

|**Parameters**|<b>cv2.CascadeClassifier.detectMultiScale(image, scaleFactor, minNeighbors, flags, minSize, maxSize)</b>|
|----------|-------------------------------------------------|
|scaleFactor | Parameter specifying how much the image size is reduced at each image scale.|
|minNeighbors| Parameter specifying how many neighbors each candidate rectangle should have to retain it.|
|minSize | Minimum possible object size. Objects smaller than that are ignored.|
|maxSize | Maximum possible object size. Objects larger than that are ignored.|

# 3- What’s new for you ?
> <ul>
> All Of Them is new for me.
> </ul>

# 4- Resources ? 

> [https://java2blog.com/cv2-videocapture-python/]
> [http://dalab.se.sjtu.edu.cn/docs/opencv_3_1_0/docs.opencv.org/3.1.0/d8/dfe/classcv_1_1VideoCapture.html#a473055e77dd7faa4d26d686226b292c1]
> [https://docs.opencv.org/3.4/db/d28/tutorial_cascade_classifier.html]
