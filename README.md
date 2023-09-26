# OpenDR datasets

This repository contains datasets collected and annotated within the scopes of the [OpenDR](https://github.com/opendr-eu/opendr) project. The datasets are read in `opendr` format, but they can also be downloaded in their raw format and used in any tool. 

## Installation and requirements

The OpenDR toolkit is an _optional_ requirement of this package, only needed if you plan to use these datasets with an OpenDR tool. For full integration, the [OpenDR](https://github.com/opendr-eu/opendr) toolkit must be installed first.

```
pip install git+https://github.com/opendr-eu/datasets.git
```

If you don't plan on using other OpenDR tools, the datasets can be downloaded from their corresponding README pages, and there is no need to install this package. 


## List of datasets

### Panoptic Segmentation

- [KITTI Panoptic Segmentation Dataset](http://panoptic.cs.uni-freiburg.de/)

KITTI panoptic segmentation dataset for urban scene understanding provides panoptic annotations for a subset of images from the KITTI Vision Benchmark Suite. The annotations for the images that we provide do not intersect with the official KITTI semantic/instance segmentation test set, therefore in addition to panoptic segmentation, they can also be used as supplementary training data for benchmarking semantic or instance segmentation tasks individually. The dataset consists of a total of 1055 images, out of which 855 are used for the training set and 200 are used for the validation set. The images are a resolution of 1280×384 pixels. We provide annotations for 11 ‘stuff’ classes and 8 ‘thing’ classes adhering to the Cityscapes ‘stuff’ and ‘thing’ class distribution.

### Object Detection 2D

- [AGI Humans in Fields dataset](examples/agi_humans)

- [TAU Engine Assembly Dataset](https://doi.org/10.5281/zenodo.7669593)

The dataset was generated by capturing 195 real images and annotating them with the correct labels (bounding boxes, keypoints and polygons). Further augmentation of the images completes the dataset to around 280,000 images. All tools and scripts to generate and replicate the dataset are provided, as well as the trained model and visualization scripts.


### Synthetic Datasets
- [Multi-view Facial Image Dataset Based on LFW](https://zenodo.org/record/5809158#.Y-JcIHZByUk)

A set of synthetically generated multi-view facial images has been created within OpenDR H2020 research project by Aristotle University of Thessaloniki based on the  LFW   image dataset which is a facial image dataset that consists of 13,233 facial images in the wild for 5,749 person identities collected from the Web. The resulting set, named AUTH-OpenDR Augmented LFW (AUTH-OpenDR ALFW), consists of 5,749 person identities. From each image of these subjects (13,233 in total), 13 synthetic images generated by yaw axis camera rotation in the interval [0◦: +60◦ ] with step +5◦ are obtained. Moreover, 10 synthetic images generated by pitch axis camera rotation in the interval [0◦ : +45◦ ] with step +5◦ are also created for each facial image of the aforementioned dataset.

- [Multi-view Facial Image Dataset Based on CelebA](https://zenodo.org/record/5809273#.Y-JdZXZByUk)

A dataset of facial images from several viewing angles was created by Aristotle University of Thessaloniki based on the CelebA image dataset, using the software that was created in OpenDR H2020 research project based on this paper and the respective code provided by the authors. CelebA is a large scale facial dataset and consists of 202,599 facial images of 10,177 celebrities captured in the wild. The new dataset namely AUTH-OpenDR Augmented CelebA (AUTH-OpenDR ACelebA) was generated from 140,000 facial images corresponding to 9161 persons, i.e. a subset of CelebA was used. For each CelebA image used, 13 synthetic images generated by yaw axis camera rotation in the interval [0◦ : +60◦ ] with step +5◦ were obtained. Moreover, 10 synthetic images generated by pitch axis camera rotation in the interval [0◦: +45◦] with step +5◦ are also created for each facial image of the aforementioned dataset. Since CelebA license does not allow distribution of derivative work we do not make AcelebA directly available but instead provide instructions and scripts on how to recreate it.

- [AUTH-OpenDR Mixed Image Annotated Dataset for Human-centric Perception Tasks](https://zenodo.org/record/5801594#.Y-TgqhxBxhE)

Realistic 3D Human models Generated from Real-World Images

This dataset contains 133 3D human models generated using the Pixel-aligned Implicit Function (PIFu) and full-body images of people from the Clothing Co-Parsing (CCP) dataset. The 3D human models are provided in .OBJ format.

Download Instructions:
`wget ftp://opendrdata.csd.auth.gr/simulation/human_data_generation_framework/human_models.tar.gz`

- [AUTH-OpenDR SMPL+D Human Bodies Dataset](https://zenodo.org/record/5801562#.Y-TgrBxBxhE)

The  dataset contains 2982 human bodies in various shapes and textures folowing the SMPL-D template. At its core, our dataset  consists of 183 unique SMPL+D bodies, which were generated through non-rigid shape registration of manually generated MakeHuman models. The rest were generated by applying shape and texture alterations to those models. In addition, we provide code for converting those human models in the FBX format.  However, pose-dependent deformations are not applied to the human models. Finally, instructions for setting a demo project in the Webots simulator are provided. In the project, one the SMPL+D models in FBX format can perform an animation from AMASS.

The dataset is available through the official GitHub repository of the OpenDR toolkit [here](https://github.com/opendr-eu/opendr/tree/master/projects/python/simulation/SMPL%2BD_human_models).

- [ActiveFace](https://github.com/opendr-eu/datasets/tree/main/active_face)

This dataset introduces a realistic synthetic facial image generation pipeline, using a modified version  of Unity's  Perception package installed on a URP project, that has been designed to support active face recognition. The developed pipeline enables generating images under a wide range of different view angles and distances, as well as under different illumination conditions and backgrounds.

The dataset is available [here](https://github.com/opendr-eu/datasets/tree/main/active_face)

- [ActiveHuman](https://zenodo.org/record/8359766)

ActiveHumans was generated using Unity’s Perception package. It consists of 175428 RGB images and their semantic segmentation counterparts taken at different environments, lighting conditions, camera distances and angles. In total, the dataset contains images for 8 environments, 33 humans, 4 lighting conditions, 7 camera distances (1m-4m) and 36 camera angles (0-360 at 10-degree intervals). Alongside each image, 2D Bounding Box, 3D Bounding Box and Keypoint ground truth annotations are also generated via the use of Labelers and are stored as a JSON-based dataset. These Labelers are scripts that are responsible for capturing ground truth annotations for each captured image or frame. Keypoint annotations follow the COCO format defined by the COCO keypoint annotation template offered in the perception package.

ActiveHuman is available [here](https://zenodo.org/record/8359766).

