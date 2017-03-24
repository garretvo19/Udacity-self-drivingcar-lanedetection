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
  The result for test images are in result_for_test_images folder 
## Pipeline for video:
    For the solidwhitelight video, the process is the same as above but I changed the vertices values. The more details are in the ipython notebook
    For the solidyellowleft video, I include the function called color_select, which selects region of images based on color threshold value. Then, I convert the selected region into grayscale image. Afterward, the process is the same, but I modify the draw_lines function. In my modified draw_line functions, I compute points on the left lane and right lane using linear interpolation
---
## Shortcomings:
    My algorithm does not work well when the lane is curved. 
---
## Possible improvements:
    Change vertices 
    Develop or implement formulations to detect curved lanes. 
  


