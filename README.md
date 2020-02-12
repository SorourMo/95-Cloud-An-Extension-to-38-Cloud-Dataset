# 95-Cloud: An Extension to 38-Cloud Dataset

95-Cloud, introduced in ([Cloud-Net+](https://arxiv.org/abs/2001.08768)), is an extension to our previously released cloud detection dataset ([38-Cloud](https://github.com/SorourMo/38-Cloud-A-Cloud-Segmentation-Dataset)). It consists of 34,701 patches of 384*384 for training. 95-Cloud's test set is exactly same as 38-Cloud's.
The training patches are extracted from 75 Landsat 8 Collection 1 Level-1 scenes mostly located in North America. 95-Cloud's test set includes 9201 patches of 20 scenes.

Each patch has 4 corresponding spectral channels which are Red (band 4), Green (band 3), Blue (band 2), and Near Infrared (band 5). Unlike other computer vision images, these channels are not combined together. Instead, they are in their correspondig directories. 

The directory tree of the dataset is exactly same as 38-Cloud.

#### *Click [here](https://vault.sfu.ca/index.php/s/CrMBgYUh1qRsHAD) for downloading the "95-Cloud training set" separately.*
#### *Click [here](https://vault.sfu.ca/index.php/s/VRzcxMyoQlBMT2D) for downloading the "95-Cloud test set" separately.*
##### *Click [here](https://www.kaggle.com/sorour/38cloud-cloud-segmentation-in-satellite-images) for downloading the "entire 38-cloud dataset (trainig+test)" through Kaggle.*

### Some Important Points:
1. Thin clouds (haze) are also considered as clouds (as well as thick clouds).
2. Natural color images are false color images used for further visualization purposes. They have not been used in the training and test phase of \[1] and \[2]\.  
3. Some of the patches do not contain useful information (many 0 pixel values). That is because of the black margins around the Landsat 8 images. The name of all 21502 informative patches (having less than 80\% black margin) are provided in training_patches_95-cloud_nonempty.csv.


More information about the dataset could be found [here](https://github.com/SorourMo/38-Cloud-A-Cloud-Segmentation-Dataset/blob/master/README.md).
**************************************
If you found this dataset useful for your research please cite these three papers:    

``` 
@INPROCEEDINGS{95-cloud,
    title={{Cloud-Net+: A Cloud Segmentation CNN for Landsat 8 Remote Sensing Imagery Optimized with Filtered Jaccard Loss Function}},
    author={S. Mohajerani and P. Saeedi},
    year={2020},
    volume={2001.08768},
    JOURNAL={arXiv},
    primaryClass={cs.CV}
}

@INPROCEEDINGS{38-cloud-1,
  author={S. {Mohajerani} and P. {Saeedi}},
  booktitle={IEEE International Geoscience and Remote Sensing Symposium (IGARSS)},
  title={Cloud-Net: An End-To-End Cloud Detection Algorithm for Landsat 8 Imagery},
  year={2019},
  volume={},
  number={},
  pages={1029-1032},
  doi={10.1109/IGARSS.2019.8898776},
  ISSN={2153-6996},
  month={July},
}

@INPROCEEDINGS{38-cloud-2,   
  author={S. Mohajerani and T. A. Krammer and P. Saeedi},   
  booktitle={IEEE 20th International Workshop on Multimedia Signal Processing (MMSP)},   
  title={{"A Cloud Detection Algorithm for Remote Sensing Images Using Fully Convolutional Neural Networks"}},   
  year={2018},    
  pages={1-5},   
  doi={10.1109/MMSP.2018.8547095},   
  ISSN={2473-3628},   
  month={Aug},  
}
