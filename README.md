# O'Donnell Research Group (ORG) Fiber Clustering White Matter Atlas

This Github repository provides an anatomically curated white matter atlas to enable consistent white matter tract parcellation across different populations ([Zhang et al. 2018](https://doi.org/10.1016/j.neuroimage.2018.06.027)). In brief, the atlas contains **an anatomical fiber tract parcellation** into 58 deep white matter tracts including major long range association and projection tracts, commissural tracts, and tracts related to the brainstem and cerebellar connections, plus 198 short and medium range superficial fiber clusters organized into 16 categories according to the brain lobes they connect. In addition, the atlas contains a **whole brain white matter parcellation** of the entire white matter into 800 fiber clusters. For more information, please see the videos, links, and related introductions on the [Atlases](http://dmri.slicer.org/atlases) page in [SlicerDMRI](http://dmri.slicer.org).

## 1. ORG Atlas Visualization

### 1.1. Visualization of the curated anatomical fiber tracts

- Download a zip file that contains all fiber tracts: [ORG-Tracts-MRB.zip](XX), ~400MB.
    - Note: Each tract is stored as an MRB file (see [here](https://www.slicer.org/wiki/Documentation/4.1/SlicerApplication/MainApplicationGUI#Medical_Reality_Bundle_.28.mrb.29_Note) for details of the MRB format in 3D Slicer). In each MRB file, there are multiple fiber clusters belonging to the tract. 
- Decompress the downloaded zip file.
- Locate an MRB file in the decompressed folder (e.g., *T_AF.mrb* for the arcuate fasciculus tract).
    - Note: The list of all anatomical tracts can be found [here](XX).
- Drag and drop the selected MRB file onto 3D Slicer for visualiztion.
    - Note: SlicerDMRI needs to be installed in 3D Slicer for this visualization (see [here](http://dmri.slicer.org/download/) for installation instructions).
    - Note: Use the Models module in 3D Slicer to visualize each indididual fiber cluster. Click the *Include Fibers* checkbox on the top left of the Models module to show the clusters in the *Scene* pannel, and then click the *eye* icon to turn on or off the visualbility of a cluster.

### 1.2. Visualization of the whole brain 800-cluster parcellation

- Download a zip file that contains the 800 fiber clusters: [ORG-800FiberClusters.zip](XX), ~500MB.
- Decompress the downloaded zip file.
- Locate the *All_clusters.mrml* file in the decompressed folder.
    - Note: This mrml file defines the 800 vtp files in the decompressed folder. Loading the mrml file will load these vtp files onto 3D Slicer.
- Drag and drop the selected mrml file onto 3D Slicer for visualiztion.
    - Note: Use the Models module in 3D Slicer to visualize each indididual fiber cluster, as described above.

### 1.3. Population mean T1/T2/b0 images

For anatomical reference, we provide the atlas population mean T1/T2/b0 images. These images are computed by transforming the T1/T2/b0 images of the 100 HCP-atlas subjects (included for the atlas generation) into the atlas space.

- Download the following images: 
    -[100HCP-population-mean-T1.nii.gz](XX), ~40MB 
    -[100HCP-population-mean-T2.nii.gz](XX), ~40MB 
    -[100HCP-population-mean-b0.nii.gz](XX), ~15MB
- Drag and drop one image (or multiple images) onto 3D Slicer for visualiztion.

## 2. Download the ORG Atlas for Subject-specific Tractography Parcellation

The ORG atlas needs to be combined with the [WhiteMatterAnalysis (WMA)](https://github.com/SlicerDMRI/whitematteranalysis) software to enable subject-specific tractography parcellation (see [here](https://github.com/SlicerDMRI/whitematteranalysis/wiki/2c\)-Running-the-Clustering-Pipeline-to-Cluster-a-Single-Subject-from-the-Atlas) for detailed instructions.)

### 2.1 Download the atlas via Python

Currently not avaiable.
<!-- ## 2. Download ORG-Atlases from github (Unsupported now). 

      git clone git@github.com:SlicerDMRI/ORG-Atlases.git

      cd ORG-Atlases
      python wm_download_anatomically_curated_atlas.py -atlas ORG-800FC-100HCP atlas_output_folder
      
      Note that Python 2.7.X needs to be installed before running this script. --> 
      
### 2.2 Download the atlas manually

- Download a zip file that contains the tractography registraion atlas: [ORG-RegAtlas-100HCP.zip](XX), ~1.2GB.
- Download a zip file that contains the fiber clustering atlas: [ORG-800FC-100HCP.zip](XX), ~600 MB.
- Decompress the downloaded zip files.

## How to cite for using the ORG atlas in your project

#### Please cite the following citations for using the atlases:

- Zhang, F., Wu, Y., Norton, I., Rathi, Y., Makris, N., O'Donnell, LJ. An anatomically curated fiber clustering white matter atlas for consistent white matter tract parcellation across the lifespan. NeuroImage, 2018 (179): 429-447
- O'Donnell, LJ., Wells III WM., Golby AJ., Westin CF. Unbiased groupwise registration of white matter tractography, in: International Conference on Medical Image Computing and Computer-Assisted Intervention, 2012 (pp. 123-130).
- O'Donnell, LJ., and Westin, C-F. Automatic tractography segmentation using a high-dimensional white matter atlas. Medical Imaging, IEEE Transactions on 2007 (26.11): 1562-1575.

#### Please include the following text (or similar) and citations for using Slicer and SlicerDMRI

- How to cite the [Slicer platform](http://wiki.slicer.org/slicerWiki/index.php/CitingSlicer)
- An example of how to cite SlicerDMRI (modify the first part of the sentence according to your use case):

    "We performed diffusion MRI tractography and/or analysis and/or visualization in 3D Slicer (www.slicer.org) via the SlicerDMRI project (dmri.slicer.org) ([Norton et al. 2017](http://cancerres.aacrjournals.org/content/77/21/e101)).

    Norton, I., Essayed, WI., Zhang, F., Pujol, S., Yarmarkovich, A., Golby, AJ., Kindlmann, G., Wassermann, D., Estepar, RSJ., Rathi, Y., Pieper, S., Kikinis, R., Johnson, HJ., Westin, C-F., and O'Donnell, LJ. SlicerDMRI: Open Source Diffusion MRI Software for Brain Cancer Research. Cancer Research 77(21), e101-e103, 2017."
