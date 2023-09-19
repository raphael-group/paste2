# PASTE2


PASTE2, the extension of PASTE, is a method for partial alignment and 3D reconstruction of spatial transcriptomics slices when they do not fully overlap in space. 

There are three main functions:
1. `src/paste2/PASTE2/partial_pairwise_align`: Given a pair of ST slices and their overlap percentage, find a partial alignment matrix. Note: In a multi-sample dataset, partial_pairwise_align should be called on each pair of adjacent slices separately.
2. `src/paste2/model_selection/select_overlap_fraction`: Decide the overlap percentage (s parameter of partial_pairwise_align) between two input ST slices. Note: In a multi-sample dataset, each pair of adjacent slices could have a different overlap percentage, hence each pair of adjacent slices might have a different estimate of s to pass to partial_pairwise_align.
3. `src/paste2/projection/partial_stack_slices_pairwise`: Given a sequence of consecutive ST slices and the partial alignments between them, project all slices onto the same 2D coordinate system. 3D reconstruction can be done by assiging a z-value to each slice.

Additionally, `src/paste2/PASTE2/partial_pairwise_align_histology` uses both gene expression and histological image information for computing the partial alignment matrix.



## Installation
We will soon make PASTE2 available on PyPi. In the mean time, you can download the repository and call the functions directly.

## Contact
If you encounter any problem running the software, please contact Xinhao Liu at xl5434@princeton.edu

## Reference
Liu, X., Zeira, R., & Raphael, B. J. (2023). Partial alignment of multislice spatially resolved transcriptomics data. Genome Research, 33(7), 1124-1132.