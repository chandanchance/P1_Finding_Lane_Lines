# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

[image2]: test_images/solidWhiteRight.jpg
[image3]: ./grayscale.jpg
[image4]: ./gaussian_blur.jpg
[image5]: ./canny.jpg
[image6]: ./result.jpg

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.


My pipeline consisted of 5 steps.

The actual image:
![alt text][image2]

## i) Grayscale

Here conversion of the image into Gray scaling takes place.(Conversion of colour image into Black and white.)

![alt text][image3]

## ii) Gaussian smoothing

For the Gray scaled image under goes smoothing so that the edge features are found better.

![alt text][image3]

## iii) Canny edge detection

Canny edge detection is used to detect the edges.

![alt text][image3]

## iv) Considering only the relavent region

Canny edge detection gives all the edges in the image out of which to select only the lane lines we need to ignore other edges. This is done by drawing a polygon. 

![alt text][image3]

## v) Hough transform and draw annotated image

To find the line segments this is applied and the lines are drawn 

![alt text][image3]

To get a solid line, draw_linesModified function has been written.



### 2. Identify potential shortcomings with your current pipeline



One potential shortcoming would be what would happen when the roads are curved. (as in optional challenge)

Another shortcoming could be the brightness. ie., if sunlight is more or when shadows are formed.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to get the brids view of the road or to use the data from maps.

Another potential improvement could be to ignore the brightness feature.
