# HaarCascade-FaceFilter

**Introduction**

HaarCascade is an algorithm to object detection by Viola-Jones paper https://www.cs.cmu.edu/~efros/courses/LBMV07/Papers/viola-cvpr-01.pdf
We will use this algorithm to detect faces, eyes or smile and put fun face filter like instagram or snapchat.




#### HaarCascade ####

**This algorithm has four stages:**

- Haar feature selection
- Compute integral image
- Adaboost Training 
- Cascade Clasifier

Haar Cascade step by step here: http://www.willberger.org/cascade-haar-explained/

This is an algorithm after Deep Learning Maybe it isn't the best but to simple tasks is a solution. 
OpenCV libray has a CascadeClassifier moudule and has too xml file to detect eyes, faces, smiles, body... We will use this library to this project.

Initialize CascadeClassifier with:

  **Classifier = cv2.CascadeClassifier(xml_file)**
  
Objetect detect:

  **Object_detected = Classifier.detect.MultiScale(image, scaleFactor, minNeighbors, minSize, maxSize)**
  
  ScaleFactor: Parameter specifying how much the image size is reduced at each image scale.
  minNeighbors: parameter specifying how many rectangles should has to retain it.
  minSize: Minimum possible object size, objects smaller than that are ignored.
  maxSize: Maximun possible object size, objects larger than that are ignored
  
  Documentation: https://docs.opencv.org/2.4/modules/objdetect/doc/cascade_classification.html
	
	
	

**Overlay**

Overlay is a tecnique to combine two images from two differnt file. So, we detect for example the eyes on image and apply overlay and we put a glasses image. To apply this tecnique we will need image with alpha channel (.PNG) and our frame we will add this channel with:

  **cv2.cvtColor(image, cv2.COLOR_BGR2BGRA)**
  
 but before apply:
  
  **cv2.imshow('frame', frame)**
  
 We will transfrom our image to RGB or BGR in openCV
  
  **cv2.cvtColor(image, cv2.COLOR_BGRA2BGR)**

I accept suggestions ..
  
