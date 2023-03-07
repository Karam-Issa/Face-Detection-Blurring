# Face-Detection-Blurring
Karam Issa  An algorithm that blurs out people's faces in any given colored image without affecting the remaining parts of the image, if any face exists. Tested using Image data set 

The algorithm uses the OpenCV library to detect faces in the image using a pre-trained classifier, and then applies a Gaussian blur to the detected faces to blur them. Here is an overview of the steps performed by the code:


1.The necessary libraries are imported, including PIL, requests, numpy, and OpenCV.

2.The input image is loaded from a specified URL using the requests library and stored in a PIL Image object.

3.The PIL Image object is converted to a NumPy array that can be processed by OpenCV using the cv2.cvtColor() function.

4.The face detection classifier is loaded from a specified file path using the cv2.CascadeClassifier() function. The haarcascade_frontalface_default.xml file is a pre-trained classifier that can detect frontal faces in images.

 **** THE  The haarcascade_frontalface_default.xml file is automatically downloaded using teh !WGET from the openCV github repo, when first running the program***
 
5.The image is converted to grayscale using the cv2.cvtColor() function, which is required for face detection.

6.The face detection classifier is applied to the grayscale image using the cv2.CascadeClassifier.detectMultiScale() function. The scaleFactor and minNeighbors parameters are used to control the sensitivity and accuracy of the face detection algorithm.

7.If any faces are detected, they are blurred using a Gaussian blur with a kernel size of (25, 25) using the cv2.GaussianBlur() function. The blurred faces are then written back to the original image array to replace the original face regions.

8.The NumPy array is converted back to a PIL Image object using the Image.fromarray() function.

9.The final output image is displayed using the display() function.


----------------------------------------------------------------------------------------------------------------------------------------------------------------Image Data set from Kaggle : https://www.kaggle.com/datasets/vin1234/count-the-number-of-faces-present-in-an-image?resource=download
About the Data set: Count the number of Faces present in an Image
Detecting instances of an object such as human faces in a picture
Total of 8196 jpg Images 
