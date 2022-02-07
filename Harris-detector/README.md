# HARRIS' detector

Implement the HARRIS’ detector using Python Notebook and Numpy.

For a fixed pair of values of the algorithm parameters (the corner response R threshold tau, k, and 5x5 Gaussian filter with sigma), measure the robustness of your implementation with synthetic images of squares corrupted by increasing amounts of Gaussian noise, as follows:  
* record the Root Mean Square (RMS) distance of the estimated corners from the true positions, and the number of spurious and missed corners;
* plot these values in three graphs, against the standard deviation of the noise;
* compare with cv2.cornerHarris from OpenCV (https://docs.opencv.org/3.0-beta/doc/py_tutorials/py_feature2d/py_features_harris/py_features_harris.html).