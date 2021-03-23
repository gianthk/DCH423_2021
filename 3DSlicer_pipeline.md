# 06.04.2021 - SXCT: from data collection to results
Lecture material for the DCH423 course - Synchrotron Radiation (SR) enabled research in Heritage Sciences and Archaeology 

### Part 5: 3D image processing hands-on session - 3DSlicer
- [X] Loading large dataset in ImageJ
- [X] Image/Show Info
- [X] Adjust pixel size (Image/Properties)
- [X] Analyze/Measure
- [X] 3D filtering (Process/Filters/Gaussian Blur)
- [X] Rescale (Image/Scale)
- [X] Save! (File/Save As/Image Sequence)
- [X] 3D ROI crop (Plugins/Stacks/Crop (3D))
- [X] Save! (File/Save As/Image Sequence)
- [X] Manual 3D ROI selection in 3DSlicer: separate VFA and MBA
    - File/Add Data
    - **Segment Editor module**
        - Add
        - **Draw**
        - Fill between slices/Initialize/Allow overlap/Apply
        - Export as STL
        - Segmentations button
        - Export to new labelmap
    - **Segmentation module**
        - Save
- [X] Automatic thresholding, logical operations and morphological refinement in 3DSlicer: bone_tissue, MBA_tissue and VFA_tissue masks
    - **Segment Editor module**
        - Add
        - **Threshold**
        - Automatic (Otsu)/Apply
        - **Islands** (Remove unconnected particles)
        - Segmentations button
        - Export to new labelmap
    - **Segmentation module**
        - Save
        - Add segment (MBA_tissue)
        - Copy MBA and bone_tissue
    - **Segment Editor module** (Segmentation: MBA_tissue)
        - **Logical operations**:
            - **Copy** bone_tissue
            - **Intersect** MBA
        - **Islands** (Remove unconnected particles)
        - **Margins** (Morphological operations)
            - **Shrink** (1x1x1)
            - **Grow** (1x1x1)
        - **Islands** (Remove unconnected particles)
            