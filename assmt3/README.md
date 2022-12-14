# Assignment 3 

## Question 1 

The algorithm can be found in the the file 'q1/q1.ipynb' 

The code prompts the user to take a 10 seconds video. The video frames are stored in the folder "video_frames". 

These frames are used for this and the subsequent questions.

I manually selected a good frame from the frame list and cropped out a region of interest (roi.png)

<img src="./q1/roi.png" width="400" />

The pattern (roi) is then used to search in 10 randomly selected images from the video frames. 

The images in which pattern is found using "Sum of squared differences" is stored in the folder "q1/pattern_match_ssd" 

The images in which pattern is found using "Normalized correlation" is stored in the folder "q1/pattern_match_ncor" 


<p float="left">
  <img src="./q1/pattern_match_ncor/16679490694421_out.png" width="400" />
  <img src="./q1/pattern_match_ssd/16679490721743_out.png" width="400" /> 
</p>


<hr />

## Question 2

The algorithm can be found in q2/q2.ipynb

The frames have been selected from the video previously recorded. 

I computed the motion function estimates and conducted image registration between consecutive frames. 

<img src="./q2/registration.png" width="400" />

<hr />

## Question 3

The algorithm can be found in q3/q3.ipynb

I first took the frames from 'video_frames' directory and appended them into a list (frame_array) in alpha-numeric order. Then

The first frame is used to find good corners. The subsequent frames use these good corners as reference points.

I created a function that plots the optical flow vectors on each frame treating every nth frame as a reference frame. By default, n is set as 1 (i.e. every previous frame).

The outputs obtained are stored in directory 'optical_flow'

> every previous frame as a reference frame

<p float="left">
  <img src="./q3/optical_flow/1.png" width="400" />
  <img src="./q3/optical_flow/1_mask.png" width="400" />
</p>

> every 11th frame as a reference frame

<p float="left">
  <img src="./q3/optical_flow/10.png" width="400" />
  <img src="./q3/optical_flow/10_mask.png" width="400" />
</p>

> every 31st frame as a reference frame

<p float="left">
  <img src="./q3/optical_flow/30.png" width="400" />
  <img src="./q3/optical_flow/30_mask.png" width="400" />
</p>

<hr />

## Question 4

The algorithm can be found in q4/q4.ipynb

I first took a few images i captured using my oak d lite camera. I cropped out the image to get the objects into frame

<p float="left">
  <img src="./q4/full_img.jpeg" width="400" />
</p>

I then took 2 objects i was interested in.

<p float="left">
  <img src="./q4/red_flower.jpeg" height="400" />
  <img src="./q4/blu_flower.jpeg" height="400" />
</p>

I created a function that detects the objects in the image.
The outputs obtained are stored in directory 'object_detected'

<p float="left">
  <img src="./q4/object_detected/blue_flower.png" width="400" />
  <img src="./q4/object_detected/red_flower.png" width="400" />
</p>

<hr />

## Question 5

The algorithm can be found in q5/q5.ipynb

The code provides option to either take live camera feed or use a prerecorded video to perform face detection.

An example output can be seen below:

<p float="left">
  <video src="./q5/video.mp4" width="400" />
  <video src="./q5/output_video.mp4" width="400" />
</p>

<hr />

## Question 6 

The algorithm can be found in q6/q6.ipynb

I Placed a marker at 50cm (T) from the camera. I then took two pictures, with the camera seperated by 6.3cm (D). 

<p float="left">
  <img src="./q6/m1.jpeg" height="400" />
  <img src="./q6/m2.jpeg" height="400" />
</p>

I first calculated the disparsity map.

<img src="./q6/disparsity.png" height="400" />

From the disparsity map, i calculated the depth map using the formula:

Depth (z) = (B * f) / Disparsity (x - x') 

<img src="./q6/depth.png" height="400" />

From the map, we find that the marker is at a distance of 47cm.