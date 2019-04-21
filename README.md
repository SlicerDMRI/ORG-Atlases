# O'Donnell Research Group (ORG) Fiber Clustering White Matter Atlas

This Github repository provides an anatomically curated white matter atlas to enable consistent white matter tract parcellation across different populations (Zhang et al. 2018). In brief, the atlas contains **an anatomical fiber tract parcellation** into 58 deep white matter tracts including major long range association and projection tracts, commissural tracts, and tracts related to the brainstem and cerebellar connections, plus 198 short and medium range superficial fiber clusters organized into 16 categories according to the brain lobes they connect. In addition, the atlas contains a **whole brain white matter parcellation** of the entire white matter into 800 fiber clusters. For more information, please see the videos, links, and related introductions on the [Atlases](http://dmri.slicer.org/atlases) page in [SlicerDMRI](http://dmri.slicer.org).

## 1. ORG Atlas Visualization

### 1.1. Visualization of the curated anatomical fiber tracts

- Download a zip file that contains all fiber tracts: [ORG-Tracts-MRB](XX), ~400MB.
    - Note: Each tract is stored as an MRB file (see [here](https://www.slicer.org/wiki/Documentation/4.1/SlicerApplication/MainApplicationGUI#Medical_Reality_Bundle_.28.mrb.29_Note) for details of the MRB format in 3D Slicer). In each MRB file, there are multiple fiber clusters belonging to the tract. 
- Decompress the downloaded zip file.
- Locate an MRB file in the decompressed folder (e.g., *T_AF.mrb* for the arcuate fasciculus tract).
    - Note: The list of all anatomical tracts can be found [here](XX).
- Drag and drop the selected MRB file onto 3D Slicer for visualiztion.
    - Note: SlicerDMRI needs to be installed in 3D Slicer for this visualization (see [here](http://dmri.slicer.org/download/) for installation instructions).
    - Note: Use the Models module in 3D Slicer to visualize each indididual fiber cluster. Click the *Include Fibers* checkbox on the top left of the Models module to show the clusters in the *Scene* pannel, and then click the *eye* icon to turn on or off the visualbility of a cluster.

### 1.2. Visualization of the whole brain 800-cluster parcellation

- Download a zip file that contains the 800 fiber clusters: [ORG-800FC-100HCP.zip](XX), ~500MB.
- Decompress the downloaded zip file.
- Locate the *All_clusters.mrml* file in the decompressed folder.
    - Note: This mrml file defines the 800 vtp files in the decompressed folder. Loading the mrml file will load these vtp files onto 3D Slicer.
- Drag and drop the selected mrml file onto 3D Slicer for visualiztion.
    - Note: Use the Models module in 3D Slicer to visualize each indididual fiber cluster, as described above.

### 1.3. Population mean T1/T2/b0 images

These population mean images are computed by transforming the T1/T2/b0 images of the 100 HCP subjects that are used for the atlas generation into the atlas space.

- Download the images: [100HCP-population-mean-T1.nii.gz](XX), ~40MB; [100HCP-population-mean-T2.nii.gz](XX), ~40MB; and [100HCP-population-mean-b0.nii.gz](XX), ~15MB, 
- Drag and drop one image (or multiple images) onto 3D Slicer for visualiztion.

## 2. Download ORG Atlas for subject-specific tractography parcellation




### 1.3. For visualization of the curated anatomical fiber tracts
    
Two atlases are available to be downloaded, including 'ORG-800FC-100HCP' and 'ORG-2000FC-100HCP'. The first one is an anatomically curated atlas including 800 fiber clusters (see blow for a list of annotated tracts in the atlas), and the second one is an uncurated atlas including 2000 fiber clusters.

* 1.1. Download the Anatomically Curated Atlas including 800 fiber clusters ([ORG-800FC-100HCP.tar.gz](https://github.com/SlicerDMRI/ORG-Atlases/releases/download/v1.0/ORG-800FC-100HCP.tar.gz), ~600 MB), and the Anatomical Tract Label for each cluster ([ORG-800FC-100HCP-MRML.tar.gz](https://github.com/SlicerDMRI/ORG-Atlases/releases/download/v1.0/ORG-800FC-100HCP-MRML.tar.gz), 270 KB).

* 1.2. Download the Tractography Registration Atlas ([ORG-RegAtlas-100HCP.tar.gz](https://github.com/SlicerDMRI/ORG-Atlases/releases/download/v1.0/ORG-RegAtlas-100HCP.tar.gz), ~1.2 GB) that is used to register a new tractography dataset to the atlas space. (This registration atlas is not necessary to be downloaded if one only wants to visualize the atlas.)

* 1.3. Download the Uncurated Atlas including 2000 fiber clusters ([ORG-RegAtlas-100HCP.tar.gz](https://github.com/SlicerDMRI/ORG-Atlases/releases/download/v1.0/ORG-RegAtlas-100HCP.tar.gz), ~1.2 GB).

<!-- ## 2. Download ORG-Atlases from github (Unsupported now). 

      git clone git@github.com:SlicerDMRI/ORG-Atlases.git

      cd ORG-Atlases
      python wm_download_anatomically_curated_atlas.py -atlas ORG-800FC-100HCP atlas_output_folder

Note that Python 2.7.X needs to be installed before running this script. --> 

## 2. Anatomical tracts annotated in the ORG-800FC-100HCP atlas. 

Except for the 7 corpus callosum (CC) tracts and the middle cerebellar peduncle (MCP) tract that cross the hemispheres (C), others are hemispheric (LR). Overall, there are 58 deep white matter fiber tracts from the association, cerebellar, commissural and projection tracts, and 16 superficial tract categories according to the brain lobes.

* Association tracts
    * arcuate fasciculus (AF) – LR
    * cingulum bundle (CB) – LR
    * external capsule (EC) – LR
    * extreme capsule (EmC) – LR
    * inferior longitudinal fasciculus (ILF) – LR
    * inferior occipito-frontal fasciculus (IoFF) – LR
    * middle longitudinal fasciculus (MdLF) – LR
    * posterior limb of internal capsule (PLIC) – LR
    * superior longitudinal fasciculus I (SLF I) – LR
    * superior longitudinal fasciculus II (SLF II) – LR
    * superior longitudinal fasciculus II (SLF III) – LR
    * uncinate fasciculus (UF) – LR

* Cerebellar tracts
    * cortico-ponto-cerebellar (CPC) – LR
    * inferior cerebellar peduncle (ICP) – LR
    * intracerebellar input and Purkinje tract (Intra-CBLM-I&P) – LR 
    * intracerebellar parallel tract (Intra-CBLM-PaT) – LR
    * middle cerebellar peduncle (MCP) – C

* Commissural tracts
    * corpus callosum 1 (CC 1) – C
    * corpus callosum 2 (CC 2) – C
    * corpus callosum 3 (CC 3) – C
    * corpus callosum 4 (CC 4) – C
    * corpus callosum 5 (CC 5) – C
    * corpus callosum 6 (CC 6) – C
    * corpus callosum 7 (CC 7) – C

* Projection tracts
    * corticospinal tract (CST) – LR
    * corona-radiata-frontal (CR-F) (excluding the CST) – LR 
    * corona-radiata-parietal (CR-P) (excluding the CST) – LR 
    * striato-frontal (SF) – LR
    * striato-occipital (SO) – LR
    * striato-parietal (SP) – LR
    * thalamo-frontal (TF) – LR
    * thalamo-occipital (TO) – LR
    * thalamo-parietal (TP) – LR

* Superficial tracts 
    * superficial-frontal (Sup-F) – LR
    * superficial-frontal-parietal (Sup-FP) – LR
    * superficial-occipital (Sup-O) – LR
    * superficial-occipital-temporal (Sup-OT) – LR
    * superficial-parietal (Sup-P) – LR
    * superficial-parietal-occipital (Sup-PO) – LR 
    * superficial-parietal-temporal (Sup-PT) – LR
    * superficial-temporal (Sup-T) – LR

## 3. Visualize the fiber clusters and the annotated anatomical fiber tracts. 

* Load output clustered_tracts.mrml file into Slicer. This will load all clusters into the scene and display a percentage of the fibers in each cluster.
* To view 100% of the fibers in all clusters (can be slow depending on the number of fibers clustered), load clustered_tracts_display_100_percent.mrml into Slicer. In this way, fibers from all 100 subjects are visualized in each cluster. Note that each cluster shows a common connection in the population and its variability across the 100 subjects.
* If downloading a pre-provided anatomically curated atlas, a mrml file that defines which clusters belonging to a certain anatomical tract (e.g. T_AF.mrml) is provided. Loading the mrml file into Slicer will visualize all clusters belonging to the anatomical tract.


**Please cite the following papers for using the atlases:**

    - Zhang, F., Wu, Y., Norton, I., Rathi, Y., Makris, N., O'Donnell, LJ. 
      An anatomically curated fiber clustering white matter atlas for consistent white matter tract parcellation across the lifespan. 
      NeuroImage, 2018 (179): 429-447
    - O'Donnell LJ., Wells III WM., Golby AJ., Westin CF. Unbiased groupwise registration of white matter tractography, 
      in: International Conference on Medical Image Computing and Computer-Assisted Intervention, 2012 (pp. 123-130).
    - O'Donnell, LJ., and Westin, CF. 
      Automatic tractography segmentation using a high-dimensional white matter atlas. 
      Medical Imaging, IEEE Transactions on 2007 (26.11): 1562-1575.

**For projects using Slicer and SlicerDMRI please also include the following text (or similar) and citations:**

* How to cite the [Slicer platform](http://wiki.slicer.org/slicerWiki/index.php/CitingSlicer)
* An example of how to cite SlicerDMRI (modify the first part of the sentence according to your use case):

    "We performed diffusion MRI tractography and/or analysis and/or visualization in 3D Slicer (www.slicer.org) via the SlicerDMRI project (dmri.slicer.org) ([Norton et al. 2017](http://cancerres.aacrjournals.org/content/77/21/e101))."
    
    - Isaiah Norton, Walid Ibn Essayed, Fan Zhang, Sonia Pujol, Alex Yarmarkovich, Alexandra J. Golby, Gordon Kindlmann, Demian Wassermann, Raul San Jose Estepar, Yogesh Rathi, Steve Pieper, Ron Kikinis, Hans J. Johnson, Carl-Fredrik Westin and Lauren J. O'Donnell. SlicerDMRI: Open Source Diffusion MRI Software for Brain Cancer Research. Cancer Research 77(21), e101-e103, 2017.
