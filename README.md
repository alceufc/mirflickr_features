MIR-Flickr Features
===================

Visual features extracted from the [MIR-Flickr images dataset](http://press.liacs.nl/mirflickr/). 

Publications
------------

If you use this set of features, please cite the MIR-Flickr dataset [as instructed here](http://press.liacs.nl/mirflickr/).
Also, please cite the paper which analyzed the extracted features:

  * Alceu Ferraz Costa, Agma Juci Machado Traina, Caetano Traina Jr., [MFS-Map: efficient context and content combination to annotate images](http://dl.acm.org/citation.cfm?id=2554868). ACM Symposium on Applied Computing (SAC), pp. 945-950, 2014. 

Features
--------

### `mirflickr_RGB_HISTOGRAM.txt`

Histogram computed by requantizing each color channel of the RGB 
color space to 7 bins yielding two 7^3 = 343 dimensional feature vectors.

### `mirflickr_HSV_HISTOGRAM.txt`

Histograms computed by requantizing each color channel of the HSV 
color space to 7 bins yielding two 7^3 = 343 dimensional feature vectors.

### `mirflickr_HSV_HIST_LAYOUT.txt`

Feature vector computed by dividing the input image 
into 3 horizontal stripes of the same height and computing a local
HSV Histogram. The local HSV histogram is computed 
by re-quantizing each color channel to 5 bins
yielding a 3 × 5^3 = 375 dimensional feature vector.

### `mirflickr_sift_100.txt`

100 bin bag-of-visual-words histogram computed by
extracting local SIFT features using a dense 
multiscale grid for sampling.

### `mirflickr_GIST.txt`

512 dimensional feature vector computed using the
Gist descriptor by resizing the image size to 256 × 256
pixels and using 8 orientations per scale.

### `mirflickr_SFTA.txt`

21 dimensional feature vector computed by 
applying the SFTA texture descriptor.

### `complete_mirflickr.txt`

Combination of all previous feature vectors.

File Format
-----------

The features are stored as text files.
Each file contains a header that ends on the line with the token `@data`.
After the token `@data`, each non-empty line contains the *feature vector*
and *annotations* of an image.
The feature vector is represented as a comma-separated list of floating point numbers.
The annotations start after the feature vector and are represented as 
comma-separated list of strings.
An image may 0 or more annotations.







