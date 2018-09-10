---
layout: post
title:  "Computer Vision"
date:   2018-9-08 21:15:05 +0000
image: /assets/images/cvbg.png

---

#### About:

Here are some MATLAB programs which explore the following different computer vision topics:
1. Image Mosaicing 
2. Optical Flow
3. Motion Detection

*Please note that I did write these programs with 1 other partner.*

#### Image Mosaicing:
[CODE](https://github.com/bpare/CV-ML/tree/master/Image_Mosaicing)

This program performs image mosaicing on two separate input images to create a final combined image.

The process of this to first find point correspondences using the Harris Corner Detection algorithm and normalized cross correlation.

Next, RANSAC is used to find a robust estimation of the homography matrix between the two images.

The homography matrix on the 2nd image is used to warped it with the first image.

Basic blending and cropping is then done order to get a more seamless final image.

Shown below is the two separate images with point correspondances matched between them:


![image1](/assets/images/cv1.png "Logo Title Text 1")


And then we have our final image composite:



![image2](/assets/images/cv2.png "Logo Title Text 1")

Bonus: Here are a few more composites created from taking pictures of wall art around Northeastern campus!

![image2](/assets/images/cv11.png "Logo Title Text 1")


![image2](/assets/images/cv12.png "Logo Title Text 1")



#### Optical Flow:
[CODE](https://github.com/bpare/CV-ML/tree/master/Optical_Flow)

This program implements the [Lucas-Kanade method](https://en.wikipedia.org/wiki/Lucas%E2%80%93Kanade_method) on two input images to create and display an optical flow field. 

The spatial intensity gradients of the second input image are calculated. Then, both images are used to determine a temporal gradient. 

Both horizontal and vertical flow components are found. This is done by by going over each pixel and solving a set of equations from a sum of product gradients in the pixel's neighborhood. 

Using these components and Matlab's quiver function, an optical flow field over the original images can be displayed.

Here is an example which shows the optical flow between two images taken from a video.

![image2](/assets/images/cv3.png "Logo Title Text 1")



![image2](/assets/images/cv4.png "Logo Title Text 1")


#### Motion Detection:
[CODE](https://github.com/bpare/CV-ML/tree/master/Motion_Detection)

This program implements a basic motion detector in MATLAB using a 1-dimensional differential operator in the temporal direction.

This operator is used to catch large temporal gradients of intensity values of individual pixels, which indicate movement in the frame.
 
The output of the differential operator is then turned into a binary mask using a threshold. 

Finally, the original frame is combined with the mask that highlights object motion to display what is moving in the frames. 

Included are options to use different combinations of 2D smoothing filters and 1D filters depending on what works best with a given input.









