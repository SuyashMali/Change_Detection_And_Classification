# Change_Detection_And_Segmentation

## Intro
This repository implements an image analysis pipeline for analyzing changes between two ortho-rectified images of the same geographical area.

The pipeline comprises several key steps:

* <b>Alignment:</b> The ORB (Oriented FAST and Rotated BRIEF) algorithm is employed for feature-based keypoint detection. Further, a homography matrix is created to wrap one of the image over other for aligining both the images.
* <b>Environmental Correction:</b> To account for variations caused by factors like time, season, or atmospheric conditions, the dark channel prior algorithm is implemented. This step normalizes the images and minimizes environmental influence on change detection.
* <b>Change Detection:</b> Morphological operations are applied to emphasize image differences and highlight potential change regions, facilitating the identification of areas with changes.
* <b>Change Segmentation:</b> Following change detection, the K-means clustering algorithm is used to categorize the identified changes into distinct classes. 

## Results

* <b>Original Images:</b>
![Original Images](assets/outputs/original_images.png)

* <b>Keypoint Matching:</b>
![Keypoint Matching](assets/outputs/keypoint_matching.png)

* <b>Comparison of Overlay of the Aligned Images and the Original Images:</b>
![Aligned Images](assets/outputs/alligned_images.png)

* <b>Environmental Haze correction using the DCP Algorithm:</b>
![Environmental Correction](assets/outputs/haze_correction.png)

* <b>Changes template post morphological operations and thresholding:</b>
![changes](assets/outputs/changes.png)

* <b>Marked Changes:</b>
![changes](assets/outputs/marked_differences.png)

* <b>Unsupervised Segmentation (Using K-Means):</b>
![changes](assets/outputs/segmented_changes.png)


## Author
Suyash Mali