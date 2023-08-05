# Document-Scanner
Computer vision/digital processing and Python 3.10 to implement a document scanner

Upload the image to be scanned as input. The frame is subsequently processed, and the desired output is then converted.
The image is duplicated and made grayscale. Using a variety of filters, such as the Gaussian filter, which is used to minimize noise in an image, the image is sharpened and any unwanted noise in the image is removed. After that, Canny edge detection is performed to the image for accurate edge detection.

The contour areas are stored in a Python list, while the calculated contour areas and corresponding contour index values are stored in a Python dictionary. The maximum area contour and its index are then found in order to determine the area of interest to be scanned in the input image.
Next, we identify the rectangle with the minimum area that fits the contour that was chosen, which is the contour with the maximum area in the image. We find the coordinates of this generated rectangle. Top left, top right, bottom left, and bottom right are the points' respective positions. Along with another set of corner points that determine the alignment or positioning of the object of interest in the final image, the points discovered are transmitted to determine the perspective transform of the image. 
