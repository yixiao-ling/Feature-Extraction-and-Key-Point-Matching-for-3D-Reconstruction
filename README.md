# CIS581-Final-Project

# Project Name

Feature Extraction and Key Point Matching for 3D Reconstruction

# What I did:
In this project, we reconstructed and visualized 3D point clouds and camera poses of 10-20 photos of two objects (Fisher Fine Arts Library and Taj Mahal) taken from different perspectives. We also localized a new query image of Taj Mahal using the reconstructed 3D map. Innovative methods such as SuperPoint, SuperGlue, DISK and LoFTR are used for feature extraction and key point matching. The performance of ensemble methods are listed and compared as well.

## To be more specific:
In the first part, we detected key features within each image that can be accurately tracked across multiple images. Then, we established good correspondences between features in different images, filtering out incorrect matches by checking for geometric consistency among the matches.
In the second part, we firstly chose pairs of images with a high number of reliable feature matches detected. From the matched features, the essential matrix is calculated. The relative pose between the cameras for the two images is then extracted from the essential matrix. Also, when combining camera intrinsics parameters (assumed to be known), we calculated the absolute camera poses. Furthermore, with the above matched feature points, we conducted triangulation to generate 3D points, which involves projecting rays from the camera centers through the feature points and finding their intersection in 3D space.


# What techniques I used:
We used different combinations of feature extraction & matching methods to find the most effective workflow for 3D reconstruction. We combined traditional methods (SIFT + KNN) with more state-of-the-art methods involving neural networks, such as LoFTR, SuperGlue and LightGlue. The performance between these ensemble methods are listed and compared as well.

We also used some tricks, such as Feature Matching with image splitting and Feature Matching with Overlap Detection. 


## Usage

For usage of 3D_library.ipynb and benchmark_experiments.ipynb, refer to the hierarchical localization (https://github.com/cvg/Hierarchical-Localization) for detailed function uses


