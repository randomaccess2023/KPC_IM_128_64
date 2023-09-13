# Information-maximization based clustering of histopathology images using deep learning

This is the repository that has the code and figures for the paper titled _**"Information-maximization based clustering of histopathology images using deep learning"**_.

> `128`, which is a folder contains models (in folder `models14`) for 14-cluster set using __128x128__ patches, script for training this particular model (`part1_kpc_cae_128_14.ipynb`), clustering output using this model (`part2_clustering.ipynb`) and umap plotting (`part3_umap.ipynb`) using latent features obtained from this model. Similarly, Folder `64` includes models (in folder `models14`) for 14-cluster set using __64x64__ patches, script for training this particular model (`part1_kpc_cae_64_14.ipynb`), clustering output using this model (`part2_clustering.ipynb`) and umap plotting (`part3_umap.ipynb`) using latent features attained from this model.
>> We have only shown these two models because they have been designated as the optimal cluster sets by internal validation metrics. By changing in one place, the scripts can be run for cluster sets using 8, 9, 10, 11, 12, 13, 15, 16, 17 and 18 as well. We mentioned where to change in the training scipts (`part1_kpc_cae_128_14.ipynb` and `part1_kpc_cae_64_14.ipynb`). Check that out.

- 'Figures' (another folder) has every figure used in the manuscript (including `Additional information` segment). Besides, some high resolution WSIs can also be found here.

- 'MODULE' folder has been used to calculate internal validation indices like __Xie-Beni index__, __Calinski-Harabasz index__, __C index__, __Dunn index__, __Hartigan index__ and __Mclain-Rao index__ for both patch sizes (__128x128__ and __64x64__ pixels). Go through these two scripts: `Internal_validation_128x128.ipynb` and `Internal_validation_64x64.ipynb` to see index calculations.

- `internal_validation_indices_plot.ipynb` has the code for creating Figure 5 as shown in the manuscript.

> `sequential_patch_creation_from_1_WSI.ipynb` stores the code for creating 18252 patches sequentially (without overlap) of size __128x128__ pixels from a randomly selected WSI with 5 stainings. We could not upload the dataset (`seq_patches_18252_from_1wsi.npy`) in GitHub because it has a size in Gigabytes. But, we have visualized the WSI that was used for sequential patch creation with 5 stainings. Additionally, we have shown a patch from this dataset with 5 stainings. A similar procedure can be followeded to create 64x64 patches with minor changes in the script but we did not do that in this research.
>> In `sequential_patch_creation_from_1wsi.ipynb`, you will notice `HE_2`, `HE_3` and `HE_4` besides `HE_1`. These `HE` series were taken for alignment and registration of images. The original tissue was sliced into a series of thin slices. Then, they were stained with `HE` and other staining methods alternately, e.g., __HE-MT-HE-CD31-HE-Ki67-HE-CK...__
>>> So, all stained images should be sandwiched by two contacts of `HE` images.  

- `IM_output_64x64_100_1.ipynb` and `IM_output_of_unused_samples_during_training.ipynb` possess the code to generate Figure 4 and Figure 5, respectively of the `Additional information` portion in the manuscript.

- `original_transformed_128x128.ipynb` has the code to visualize the original and transformed versions of a patch (__128x128__ pixels). Look over Figure 2 of the `Additional information` division in the paper.

- `the_learning_curve.ipynb` contains the code to create Figure 3 of the `Additional information` segment in the typescript.

> `patch_visualization_128x128_64x64.ipynb` has the code to create Figure 1 of the manuscript. In addition, we have shown first 20 samples of both datasets (`slice128_Block2_20K.npy` ---> contains __128x128__ patches and 'slice64_Block2_20K.npy' ---> stores __64x64__ patches) with 5 stainings. The sizes of `slice128_Block2_20K.npy` and `slice64_Block2_20K.npy` are not suitable for being uploaded in GitHub (_Gigabyte_ files).
>> But, these two datasets can be found in this link: [Location of __128x128__ and __64x64__ patches](https://figshare.com/articles/dataset/Random_patches_from_histopathological_images_of_KPC_mouse/24129360)

- `histogram_colormap_WSI.ipynb` keeps the code to create Figure 10 of the manuscript.

#### `filename_tif8_block2.txt` contains the addresses of 191 WSIs.

- By using `random_patch_creation.ipynb` script, randomly patches can be created from 191 WSIs. Here, we have presented the code for creating __128x128__ patches but with minor changes, __64x64__ patches can also be created. We indicated where to change in the script to create __64x64__ patches.
