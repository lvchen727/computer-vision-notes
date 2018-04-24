# computer-vision-notes

## CV basics
#### [image filtering](https://www.cs.cornell.edu/courses/cs6670/2011sp/lectures/lec02_filter.pdf)

1. low-pass filtering for image smoothing and noise reduction 
	- [spatial averaging](http://fourier.eng.hmc.edu/e161/lectures/smooth_sharpen/node1.html)
	- Guassian filter (non-uniform low-pass filter)
		* [guassian filter note1](https://homepages.inf.ed.ac.uk/rbf/HIPR2/gsmooth.htm)
		* [guassian filter note2](https://www.cs.auckland.ac.nz/courses/compsci373s1c/PatricesLectures/Gaussian%20Filtering_1up.pdf)
	- [why use Guassian filter for imaging processing](https://dsp.stackexchange.com/questions/3002/why-are-gaussian-filters-used-as-low-pass-filters-in-image-processing)

2. high-pass filtering for enhancing and edge detection
	- [Laplacian of Guassian (LoG)](http://fourier.eng.hmc.edu/e161/lectures/gradient/node8.html)
	- [Difference of Guassian (DoG)](http://fourier.eng.hmc.edu/e161/lectures/gradient/node8.html)
		* G is a close approximate to scale-normalized LoG.
		

#### [image gradient](http://www.cs.cmu.edu/~16385/s17/Slides/4.0_Image_Gradients_and_Gradient_Filtering.pdf)

#### [guassian and Laplacian pyramid](http://www.cs.toronto.edu/~mangas/teaching/320/slides/CSC320L10.pdf)


## Feature descriptors

#### [Scale Invariant Feature Transform(SIFT)](https://www.cs.ubc.ca/~lowe/papers/ijcv04.pdf)

There are two parts for SIFT:
- Part I: locate SIFT detectors(keypoints)
	1. Scale-space extrema detection: arch over multiple scales and image locations
	2. Keypoint localization:  a model to detrmine location and scale.      
	3. Orientation assignment: mpute best orientation(s) for each keypoint region.
- [Part II: compute feature descriptor](http://aishack.in/tutorials/sift-scale-invariant-feature-transform-features/)
	4. Keypoint description: e local image gradients at selected scale and rotation to describe each keypoint region.

		SIFT computes the descriptor by taking a 16x16 block of pixels centered at a key point, dividing it into 4x4 cells, and computing an 8-bin histogram of gradient orientations within each cell(the length of each arrow corresponding to the sum of the gradient magnitudes near that direction within the region using "guassian weighted function"). This results in a 4*4*8=128-element vector, which is the descriptor.



Great notes:
- [SIFT note1 ](https://courses.cs.washington.edu/courses/cse576/06sp/notes/Interest2.pdf)
- [SIFT note2 ](http://aishack.in/tutorials/sift-scale-invariant-feature-transform-introduction/)
- [vl_feat sift](http://www.vlfeat.org/api/sift.html)
- [vl_feat dsift](http://www.vlfeat.org/api/dsift.html)

#### Histogram of Oriented Gradients(HOG)
- [vl_feat hog](http://www.vlfeat.org/api/hog.html)


#### CNN


## Feature encoders

#### BOVW

#### FV


## References
- [computer Image Processing and Analysis (E161)](http://fourier.eng.hmc.edu/e161/)
- [Image processing learning resources](https://homepages.inf.ed.ac.uk/rbf/HIPR2/)
- [An interative Guide to Fourier Transform](https://betterexplained.com/articles/an-interactive-guide-to-the-fourier-transform/)
- [ComputerVision CMU](http://www.cs.cmu.edu/~16385/s17/) - This one is really interesting!
- Optical character recognition (OCR)

# computer-vision-notes

## CV basics
#### [image filtering](https://www.cs.cornell.edu/courses/cs6670/2011sp/lectures/lec02_filter.pdf)

1. low-pass filtering for image smoothing and noise reduction 
	- [spatial averaging](http://fourier.eng.hmc.edu/e161/lectures/smooth_sharpen/node1.html)
	- Guassian filter (non-uniform low-pass filter)
		* [guassian filter note1](https://homepages.inf.ed.ac.uk/rbf/HIPR2/gsmooth.htm)
		* [guassian filter note2](https://www.cs.auckland.ac.nz/courses/compsci373s1c/PatricesLectures/Gaussian%20Filtering_1up.pdf)
	- [why use Guassian filter for imaging processing](https://dsp.stackexchange.com/questions/3002/why-are-gaussian-filters-used-as-low-pass-filters-in-image-processing)

2. high-pass filtering for enhancing and edge detection
	- [Laplacian of Guassian (LoG)](http://fourier.eng.hmc.edu/e161/lectures/gradient/node8.html)
	- [Difference of Guassian (DoG)](http://fourier.eng.hmc.edu/e161/lectures/gradient/node8.html)
		* G is a close approximate to scale-normalized LoG.
		

#### [image gradient](http://www.cs.cmu.edu/~16385/s17/Slides/4.0_Image_Gradients_and_Gradient_Filtering.pdf)

#### [guassian and Laplacian pyramid](http://www.cs.toronto.edu/~mangas/teaching/320/slides/CSC320L10.pdf)


## Feature descriptors

#### [Scale Invariant Feature Transform(SIFT)](https://www.cs.ubc.ca/~lowe/papers/ijcv04.pdf)

There are two parts for SIFT:
- Part I: locate SIFT detectors(keypoints)
	1. Scale-space extrema detection: arch over multiple scales and image locations
	2. Keypoint localization:  a model to detrmine location and scale.      
	3. Orientation assignment: mpute best orientation(s) for each keypoint region.
- [Part II: compute feature descriptor](http://aishack.in/tutorials/sift-scale-invariant-feature-transform-features/)
	4. Keypoint description: e local image gradients at selected scale and rotation to describe each keypoint region.

		SIFT computes the descriptor by taking a 16x16 block of pixels centered at a key point, dividing it into 4x4 cells, and computing an 8-bin histogram of gradient orientations within each cell(the length of each arrow corresponding to the sum of the gradient magnitudes near that direction within the region using "guassian weighted function"). This results in a 4*4*8=128-element vector, which is the descriptor.



Great notes:
- [SIFT note1 ](https://courses.cs.washington.edu/courses/cse576/06sp/notes/Interest2.pdf)
- [SIFT note2 ](http://aishack.in/tutorials/sift-scale-invariant-feature-transform-introduction/)
- [vl_feat sift](http://www.vlfeat.org/api/sift.html)
- [vl_feat dsift](http://www.vlfeat.org/api/dsift.html)

#### Histogram of Oriented Gradients(HOG)
- [vl_feat hog](http://www.vlfeat.org/api/hog.html)


#### CNN


## Feature encoders

#### BOVW

#### FV


## References
- [computer Image Processing and Analysis (E161)](http://fourier.eng.hmc.edu/e161/)
- [Image processing learning resources](https://homepages.inf.ed.ac.uk/rbf/HIPR2/)
- [An interative Guide to Fourier Transform](https://betterexplained.com/articles/an-interactive-guide-to-the-fourier-transform/)
- [ComputerVision CMU](http://www.cs.cmu.edu/~16385/s17/) - This one is really interesting!
- Optical character recognition (OCR)

