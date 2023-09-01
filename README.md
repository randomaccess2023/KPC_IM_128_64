# KPC_IM_128_64

This folder contains code and figures for the paper titled "Information-maximization based clustering of histopathology images using deep learning".

Folder '128' contains models (in folder 'models14') for 14-cluster set using 128x128 patches, script for training this particular model ('part1_kpc_cae_128_14.ipynb'), clustering output using this model ('part2_clustering.ipynb') and umap plotting ('part3_umap.ipynb') using latent features for this model. Similarly, Folder '64' contains models (in folder 'models14') for 14-cluster set using 64x64 patches, script for training this particular model ('part1_kpc_cae_64_14.ipynb'), clustering output using this model ('part2_clustering.ipynb') and umap plotting('part3_umap.ipynb') using latent features for this model. We have only shown these two models because have been determined as the optimal cluster sets by internal validation. By changing in one place, the scripts can be run for cluster sets using 8, 9, 10, 11, 12, 13, 15, 16, 17 and 18 as well. We have mentioned where to change in the training scipts ('part1_kpc_cae_128_14.ipynb' and 'part1_kpc_cae_64_14.ipynb'). Check that out.

Folder 'Figures' contains every figure used in the main manuscript and additional information section of the paper. Besides, some high resolution WSIs can also be found here.

'MODULE' folder has been used to calculate internal validation indices like Xie-Beni index, Calinski-Harabasz index, C index, Dunn index, Hartigan index and Mclain-Rao index for both patch sizes (128x128 and 64x64). Check these two scripts: 'Internal_validation_128x128.ipynb' and 'Internal_validation_64x64.ipynb' to see index calculation.

'internal_validation_indices_plot.ipynb' has the code for creating Figure 5 in the main manuscript.

'sequential_patch_creation_from_1_WSI.ipynb' stores the code for creating 18252 patches sequentially of size 128x128 from a randomly selected WSI with 5 stainings. We could not upload the dataset ('seq_patches_18252_from_1wsi.npy') in GitHub because it has a size of 4.49 GB. But, we have visualized the WSI that was used for sequential patch creation with 5 stainings. Additionally, we have shown a patch from this dataset with 5 stainings. Same procudure can be repeated to create 64x64 patches with minor changes in the script but we didn't show that to avoid repetitiveness.

'IM_output_64x64_100_1.ipynb' and 'IM_output_of_unused_samples_during_training.ipynb' contain the code to generate Figure 4 and Figure 5, respectively of additional information section in the paper.

'original_transformed_128x128.ipynb' has the code to visualize the original and transformed version of a patch of size 128x128. Check Figure 2 of additional information section in the paper.

'the_learning_curve.ipynb' contains the code to create Figure 3 of additional information section in the paper.

'patch_visualization_128x128_64x64.ipynb' has the code to create Figure 1 of the main manuscript in the paper. In addition, we have shown first 20 samples of both datasets ('slice128_Block2_20K.npy' ---> contains 128x128 patches and 'slice64_Block2_20K.npy' ---> contains 64x64 patches) with 5 stainings because the size of 'slice128_Block2_20K.npy' (7.86 GB) and 'slice64_Block2_20K.npy' (1.97 GB) are not suitable to be uploaded in GitHub.

'histogram_colormap_WSI.ipynb' has the code to create Figure 10 of the main manuscript in the paper.

'filename_tif8_block2.txt' contains the addresses of 191 WSIs.

By using 'random_patch_creation.ipynb' script, randomly patches can be created from 191 WSIs. Here, we have presented code for creating 128x128 patches but with minor changes, 64x64 patches can also be created. We have mentioned where to change in the script to create 64x64 patches. Additionally, We have shown the WSIs in Figure 2 of the main manuscript in the paper also.
