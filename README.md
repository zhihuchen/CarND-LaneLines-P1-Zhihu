#**Finding Lane Lines on the Road** 


### Reflection (Writeup)

###1. Description of the pipeline 

* Covert RGB image to gray scale image.

* Use Gaussian Blur to smooth the image.

* Run the Canny edge detection.

* Convert the edge to Hough space.

* Define a mask function.

* Average the lines from Hough output lines. Here one polynomial is derived from the average to denote the left and right lane.

* draw_line() function then will draw the new averaged left and right lines.

* Line polynomial are smoothed from the previous frames. Here a smoothing filter is applied.

* Draw the lane on the image



###2.Potential shortcomings of the pipeline

- Algorithm shortcomings:

 - The masking parameters are just defined as fixed varibles.

- Code Engineering shortcomings:

 - The varibles are passed through the frames are global variables. These will cause unexpected troubles in debugging in the future.


###3. Possible improvements 

- The challenge video is not working for the current algorithm

- Dynamic masking function.

- Fitting 3 degree ploynomial line functions from Hough lines output
