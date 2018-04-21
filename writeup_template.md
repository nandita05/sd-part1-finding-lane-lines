# **Finding Lane Lines on the Road** 

## Writeup Template

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

The lane pipline creation process consisted of a list of steps. 

Initially I imported packages which would be required to call helper functions. 
Upon iterating on all images inside the test_images folder, I performed various opertations on each one of them.

First step was to convert images to Grayscale so that identification of edges would become easier. 
Then I applied Gaussian blur to elimiate blurry areas, and canny function to identify the bright edges. 
After this step, depending on the image's shape :height and width, I defined my area of interest by defining vertices.

Then I used predefined hough_lines function to draw hough lines along the region of interest.
After this, I copied the images with pipeline on lanes in output folder.

After doing this for eachof the test images, I used the function process_image to work on the solidRightWhite and solidYellowLeft videos. 


![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One  shortcoming is the pipeline does not detect the curved lines properly whenever the road is turning. 
Also the detected lines also tend to merge sometimes at the end and are flickery


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...
Find a method to enable detection of line when the road bends and in different terrains.
