# KPC_IM_128_64

This folder contains code and figures for the paper titled "Information-maximization based clustering of histopathology images using deep learning".

Folder '128' contains models (in folder 'models14') for 14-cluster set using 128x128 patches, script for training this particular model ('part1_kpc_cae_128_14.ipynb'), clustering output using this model ('part2_clustering.ipynb') and umap plotting ('part3_umap.ipynb') using latent features for this model. Similarly, Folder '64' contains models (in folder 'models14') for 14-cluster set using 64x64 patches, script for training this particular model ('part1_kpc_cae_64_14.ipynb'), clustering output using this model ('part2_clustering.ipynb') and umap plotting('part3_umap.ipynb') using latent features for this model. By changing one place, the scripts can be run for cluster sets using 8, 9, 10, 11, 12, 13, 15, 16, 17 and 18 as well. We have mentioned where to change in the training scipts ('part1_kpc_cae_128_14.ipynb' and 'part1_kpc_cae_64_14.ipynb'). Check that out.

Folder 'Figures' contains every figure used in the main manuscript and additional information section of the paper. Besides, some high resolution WSIs can also be found here.

'MODULE' folder has been used to calculate internal validation indices like Xie-Beni index, Calinski-Harabasz index, C index, Dunn index, Hartigan index and Mclain-Rao index for both patch sizess(128x128 and 64x64). Check these two scripts: 'Internal_validation_128x128.ipynb' and 'Internal_validation_64x64.ipynb' to see index calculation.

'internal_validation_indices_plot.ipynb' has the code for creating Figure 5 in the main manuscript.

'sequential_patch_creation_from_1_WSI.ipynb' stores the code for creating 18252 patches sequentially of size 128x128 from a randomly selected WSI with 5 stainings. We could not upload the dataset ('seq_patches_18252_from_1wsi.npy') in GitHub because it has a size of 4.49 GB. But, we have visualized the WSI that was used for sequential patch creation with 5 stainings. Additionally, we have shown a patch with from this dataset with 5 stainings. 
