#**Finding Lane Lines on the Road** 

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

###1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 8 steps. 

1. I made a copy of the image and used it afterwards.

2. I converted the image to grayscale.

3. I found the edges using canny edge detection.

4. I defined a region of interest and only care about the edges in that region.

5. I used hough transformation to find the line segments.

6. I divided the line segments into left lines and right lines.

7. For each side of line segements, I calculated the weighted average slope and intercept.

8. I drew the line in the region of interest based on the slope and intercept I found.

In order to draw a single line on the left and right lanes, I did not modify the draw_lines() function but passed the end points of each line to this function.

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


###2. Identify potential shortcomings with your current pipeline

One potential shortcoming would be what would happen when the lane is a curve.

Another shortcoming could be the line vibrates a lot when the lane is not continuous.


###3. Suggest possible improvements to your pipeline

A possible improvement would be to use polyfit to finish the optional challenge.

Another potential improvement could be to try different combinations of parameters to have a better model to deal with lanes.
