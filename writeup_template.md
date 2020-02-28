# **Finding Lane Lines on the Road** 


### Reflection

### 1. Pipeline


1. Convert the image to grayscale and apply gaussian smoothing to the image
2. Use Canny edge detector and mark the region of interest
3. In order to draw lines on the image, filter the lines based on the slope values and assign line coordinates to left and right lines.
4. Find the average value of the slopes and the average values of the coordinates of right and left lines to be drawn to prevent flickering  in a video stream
5. Convert the points in image space to lines in hough space
6. Use regression to compute the slope, intercept and the unkown coordinates
7. Draw lines on the image





### 2. Potential shortcomings and possible improvements

1. In this pipeline, vertices in ROI were hardcoded and the value for slope condition was selected on a trial and error basis. This is usually unfavorable and there has to be a way to optimize and choose the optimum values real time.
2. Finding lanes during the night would be a challenge due to color recognition.
3. There has to be a way in which ROI can be chosen based on the height of the camera integrated into the vehicle.
4. Cameras alone don't really perform well in weather conditions such as rain, fog or snow. Integration of another sensor makes it robust.
5. The lane lines drawn in the video stream suffer from flickering at times. Smoothing/filtering can reduce this behavior.


