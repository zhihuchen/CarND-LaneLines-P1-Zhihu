#**Finding Lane Lines on the Road** 


### Reflection

###1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

* Covert RGB image to gray scale image.

* Use Gaussian Blur to smooth the image.

* Run the Canny edge detection.

* Convert the edge to Hough space.

* Define a mask function.

* Average the lines from Hough output lines. Here one polynomial is derived from the average to denote the left and right lane.

* draw_line() function then will draw the new averaged left and right lines.

* Line polynomial are smoothed from the previous frames. Here a smoothing filter is applied.

* Draw the lane on the image



###2. Identify potential shortcomings with your current pipeline

- Algorithm shortcomings:

- The masking parameters are just defined as fixed varibles.

- Code Engineering shortcomings:

- The varibles are passed through the frames are global variables. These will cause unexpected troubles in debugging in the future.


###3. Suggest possible improvements to your pipeline

- The challenge video is not working for the current algorithm

- Dynamic masking function.

- Fitting 3 degree ploynomial line functions from Hough lines output
