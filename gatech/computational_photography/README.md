## Computational Photography

GA Course Link: https://omscs.gatech.edu/cs-6475-computational-photography


### Access to Code

Instructions [here](../README.md)


### Course Overview

_This class explores how computation impacts the entire workflow of photography, which is traditionally aimed at capturing light from a (3D) scene to form a (2D) image. A detailed study of the perceptual, technical and computational aspects of forming pictures, and more precisely, the capture and depiction of reality on a (mostly 2D) medium of images, is undertaken over the entire term. The scientific, perceptual, and artistic principles behind image-making will be emphasized, especially as impacted and changed by computation. Topics include the relationship between pictorial techniques and the human visual system; intrinsic limitations of 2D representations and their possible compensations; and technical issues involving capturing light to form images. Technical aspects of image capture and rendering, and exploration of how such a medium can be used to its maximum potential, will be examined. New forms of cameras and imaging paradigms will be introduced._


### Projects


#### Weekly Assignments

The weekly assignments for this course span creating a homemade pinhole camera to implementing panorama and HDR algorithms. The code for these assignments are not included (either here or on the Drive site), but the results can be seen in the [portfolio pdf](comp_photo_portfolio.pdf).


#### Mid Term

The midterm involved replicating the results of the Avidan &amp; Shamir paper [_Seam Carving for Content-Aware Image Resizing_](https://perso.crans.org/frenoy/matlab2012/seamcarving.pdf). he major premise of the work is that the ‘visually’ optimal means for scaling (retargeting) an image is to utilize low energy (non-edge pixels) flat regions of the image but contain​ ​the​ ​path​ ​to​ ​be​ ​spatially​ ​consistent​ ​(follow​ ​a​ ​contiguous​ ​seam). The paper implements a fast Dynamic Programming algorithm for implementing image retargeting. 


#### Final Project

In the final project I attempted to replicate of the Rubinstein et al. paper [_Improved Seam Carving for Video Retargetting_](http://www.eng.tau.ac.il/~avidan/papers/vidret.pdf). The paper implements image retargetting over 3-dimentionsal video cubes (XY-Time). The paper utilizes a graph-cut algorithm for finding the low energy "seam" to extract. In addition, it presents an _improved_ algorithm for finding low energy seams.

Although I correctly reimplemented the paper in 2-dimensions, the paper utilized "zoning" a "sleeve" of pixels out of the video cube for retargetting by downsampling the video. The video resample was only implemented in the XY access, resulting in slow seam extraction as well as lack luster results. In 2D, I validated that the results obtained match the Avidan &amp; Shamir in 2D suggesting that the graph cut algorithm was correctly implemented. Without the time pressure of academia, this is a case where it would have been nice to revisit the code / problem again.
