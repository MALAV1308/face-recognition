# HOW TO RUN


First, incase you don't already have any dataset of faces. Use the script create_dataset.py. This would prompt you with a request to enter the name of the person you want to recognize.

After this is done, it creates a folder title ('The name of the person'), with images of the person inside the folder.
The folder name 'Unknown' are used to place a bounding box on people we do not yet know.

### python create_dataset.py



Second, you need to run the extract_embedding.py script. What this does is, base on your dataset. We want to find a unique way of representing those, image of each person. Simply, selecting the important features of a person. Instead of using the original size of the image, we would rather convert it into a 128-Dimension feature vector, which is much easier to use in training our machine learning model. 

### python extract_embeddings.py



Thridly, Base on the previous file, we stored the features according to their represented labels.
so for example [(128, 1), name_of_the_person] in a binary file, which would be used for recognition later. If another person is being added to the database, make sure you repeat the whole process from the top.

Finally to recognize, a person on an image or video run the scripts below, and change the file path to where these files can be found.

###python recognize_image.py (for images)
###python recognize_video_file (for videos)


Incase you want to use the web camera, to perform live recognition, use the script recognize_camera.py


###python recognize_camera.py


### Note, Since these files are too large to be uploaded on github, you may find them in the links below. Please put all these files once downloaded into the folder called /model.

Link are here : https://github.com/spmallick/learnopencv/tree/master/FaceDetectionComparison/models

The name of these files are deploy.prototxt, opencv_face_detector.pbtxt, opencv_face_detector_uint8.pb, res10_300x300_ssd_iter_140000.caffemodel and haarcascade_frontalface_default.xml.