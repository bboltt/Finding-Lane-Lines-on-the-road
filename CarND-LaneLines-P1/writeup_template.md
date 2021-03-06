# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/laneLines_thirdPass.jpg 

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 step
First, I converted the images to grayscale.
Second, applies Gaussian smmothingh.
Third, applies Canny transform.
Foutth, applies region of interest.
Fifth, applies Hough transform.
Sixth, draw red lines. 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by separating right lines and left lines by identifying if the slope is positive. Then Find endpoints to draw the extented lines.

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


There are a few moments the noise red line flashing out. And it is acrosss the screen.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to make the lines stable.
