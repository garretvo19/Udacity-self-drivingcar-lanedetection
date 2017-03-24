#**Write up for the first project** 
## This is the write-up for the first project: lane detection. 

In this write-up, I will include the following:
  1. Project pipeline
  2. Short-comings
  3. Possible Improvement
----  
 ## Project pipeline
 I have two ipython notebooks. One is for testing images, and one is for videos. They are as following:
  ## Pipeline for testing images:
  1. Read through a sequence of test images
  2. Convert all of them to grayscale image
  3. Perform Gaussian smoothing with kernel size = 5
  4. Perform canny edge detection with low threshold = 50 and high threshold = 150
  5. Re-define the region of interest function (ROI) with vertices values based on the lectures but slightly change 450->460, 290->320, 290->310
  6. Then, I apply the ROI function to result from canny edge detection
  7. Use the hough line transform and draw line functions to draw the lane 
  8. Plot the detected lane on the original image
## Pipeline for video 

