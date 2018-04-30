# org-atlases
O'Donnell Research Group (ORG) Fiber Clustering White Matter Atlases

**Please cite the following papers:**

    Zhang, F., Wu, Y., Norton, I., Rathi, Y., Makris, N., O’Donnell, L.J., 2018. 
    A data­-driven groupwise fiber clustering atlas for consistent white matter parcellation and anatomical tract identification of subjects across the lifespan, 
    in: Annual Meeting of the International Society for Magnetic Resonance in Medicine (ISMRM).

**For projects using Slicer please also include this text (or similar):**

    "We performed tractography visualization with anatomical hierarchies in 3D Slicer (http://www.slicer.org)
    via the SlicerDMRI project (https://github.com/SlicerDMRI), funded by NIH U01 CA199459."

# Installation
## 1. Download ORG-Atlases from github. 

      git clone git@github.com:SlicerDMRI/ORG-Atlases.git

## 2. Download a pre-provided atals using the provided script ''wm_download_anatomically_curated_atlas.py'', as follows:

      
      cd ORG-Atlases
      python wm_download_anatomically_curated_atlas.py -atlas ORG-800FC-100HCP atlas_output_folder

Note that Python 2.7.X needs to be installed before running this scirpt.

## 3. Visualize the fiber clusters and the annotated anatomical fiber tracts. 

* Load output clustered_tracts.mrml file into Slicer. This will load all clusters into the scene and display a percentage of the fibers in each cluster.
* To view 100% of the fibers in all clusters (can be slow depending on the number of fibers clustered), load clustered_tracts_display_100_percent.mrml into Slicer.
* If downloading a pre-provided anatomically curated atlas, a mrml file that defines which clusters belonging to a certain anatomical tract (e.g. T_AF.mrml) is provided. Loading the mrml file into Slicer will visualize all clusters belonging to the anatomical tract.
