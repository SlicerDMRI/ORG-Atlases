# org-atlases
O'Donnell Research Group (ORG) Fiber Clustering White Matter Atlases

**Please cite the following papers for using the atlases:**

    Zhang, F., Wu, Y., Norton, I., Rathi, Y., Makris, N., O'Donnell, LJ. 
    A data-driven groupwise fiber clustering atlas for consistent white matter parcellation and anatomical tract identification of subjects across the lifespan, 
    in: Annual Meeting of the International Society for Magnetic Resonance in Medicine (ISMRM), 2018.
    
    O'Donnell LJ., Wells III WM., Golby AJ., Westin CF. 
    Unbiased groupwise registration of white matter tractography, 
    in: International Conference on Medical Image Computing and Computer-Assisted Intervention 2012 Oct 1 (pp. 123-130). Springer Berlin Heidelberg.
    
    O'Donnell, LJ., and Westin, CF. 
    Automatic tractography segmentation using a high-dimensional white matter atlas. 
    Medical Imaging, IEEE Transactions on 26.11 (2007): 1562-1575.

**For projects using Slicer and SlicerDMRI please also include the following text (or similar) and citations:**

* How to cite the [Slicer platform](http://wiki.slicer.org/slicerWiki/index.php/CitingSlicer)
* An example of how to cite SlicerDMRI (modify the first part of the sentence according to your use case):

    "We performed diffusion MRI tractography and/or analysis and/or visualization in 3D Slicer (www.slicer.org) via the SlicerDMRI project (dmri.slicer.org) (Norton et al. 2017)."
    
    - [Isaiah Norton, Walid Ibn Essayed, Fan Zhang, Sonia Pujol, Alex Yarmarkovich, Alexandra J. Golby, Gordon Kindlmann, Demian Wassermann, Raul San Jose Estepar, Yogesh Rathi, Steve Pieper, Ron Kikinis, Hans J. Johnson, Carl-Fredrik Westin and Lauren J. O'Donnell. SlicerDMRI: Open Source Diffusion MRI Software for Brain Cancer Research. Cancer Research 77(21), e101-e103, 2017.](http://cancerres.aacrjournals.org/content/77/21/e101)


# Installation
## 1. Download ORG-Atlases from github. 

      git clone git@github.com:SlicerDMRI/ORG-Atlases.git

## 2. Download a pre-provided atlas using the provided script ''wm_download_anatomically_curated_atlas.py'', as follows:

      cd ORG-Atlases
      python wm_download_anatomically_curated_atlas.py -atlas ORG-800FC-100HCP atlas_output_folder

Two atlases are available to be downloaded (-atlas), including 'ORG-800FC-100HCP' and 'ORG-2000FC-100HCP'. The second one is an anatomically curated atlas including 800 fiber clusters, and the second one is an uncurated atlas including 2000 fiber clusters.

Note that Python 2.7.X needs to be installed before running this script.

## 3. Visualize the fiber clusters and the annotated anatomical fiber tracts. 

* Load output clustered_tracts.mrml file into Slicer. This will load all clusters into the scene and display a percentage of the fibers in each cluster.
* To view 100% of the fibers in all clusters (can be slow depending on the number of fibers clustered), load clustered_tracts_display_100_percent.mrml into Slicer. In this way, fibers from all 100 subjects are visualized in each cluster. Note that each cluster shows a common connection in the population and its variability across the 100 subjects.
* If downloading a pre-provided anatomically curated atlas, a mrml file that defines which clusters belonging to a certain anatomical tract (e.g. T_AF.mrml) is provided. Loading the mrml file into Slicer will visualize all clusters belonging to the anatomical tract.
