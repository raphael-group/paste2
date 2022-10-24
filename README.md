# PASTE2


PASTE2, the extension of PASTE, is a method for partial alignment and 3D reconstruction of spatial transcriptomics slices when they do not fully overlap in space. 

There are three main functions:
1. `src/paste2/PASTE2/partial_pairwise_align`: Given a pair of ST slices and their overlap percentage, find a partial alignment matrix. 
2. `src/paste2/model_selection/decide_overlap`: Decide the overlap percentage (s parameter of partial_pairwise_align) between two input ST slices.
3. `src/paste2/projection/partial_stack_slices_pairwise`: Given a sequence of consecutive ST slices and the partial alignments between them, project all slices onto the same 2D coordinate system. 3D reconstruction can be done by assiging a z-value to each slice.

Additionally, `src/paste2/PASTE2/partial_pairwise_align_histology` uses both gene expression and histological image information for computing the partial alignment matrix.



### Installation
We will soon make PASTE2 available on PyPi. In the mean time, you can download the repository and call the functions directly.
