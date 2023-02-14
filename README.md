# OpenDR datasets

This repository contains datasets collected and annotated within the scopes of the [OpenDR](https://github.com/opendr-eu/opendr) project. The datasets are read in `opendr` format, but they can also be downloaded in their raw format and used in any tool. 

## Installation and requirements

The OpenDR toolkit is an _optional_ requirement of this package, only needed if you plan to use these datasets with an OpenDR tool. For full integration, the [OpenDR](https://github.com/opendr-eu/opendr) toolkit must be installed first.

```
pip install git+https://github.com/opendr-eu/datasets.git
```

If you don't plan on using other OpenDR tools, the datasets can be downloaded from their corresponding README pages, and there is no need to install this package. 


## List of datasets

### Object Detection 2D

- [AGI Humans in Fields dataset](examples/agi_humans)

### Synthetic Datasets
- [Multi-view Facial Image Dataset Based on LFW](https://zenodo.org/record/5809158#.Y-JcIHZByUk)

A set of synthetically generated multi-view facial images has been created within OpenDR H2020 research project by Aristotle University of Thessaloniki based on the  LFW   image dataset which is a facial image dataset that consists of 13,233 facial images in the wild for 5,749 person identities collected from the Web. The resulting set, named AUTH-OpenDR Augmented LFW (AUTH-OpenDR ALFW), consists of 5,749 person identities. From each image of these subjects (13,233 in total), 13 synthetic images generated by yaw axis camera rotation in the interval [0◦: +60◦ ] with step +5◦ are obtained. Moreover, 10 synthetic images generated by pitch axis camera rotation in the interval [0◦ : +45◦ ] with step +5◦ are also created for each facial image of the aforementioned dataset.

- [Multi-view Facial Image Dataset Based on CelebA](https://zenodo.org/record/5809273#.Y-JdZXZByUk)

A dataset of facial images from several viewing angles was created by Aristotle University of Thessaloniki based on the CelebA image dataset, using the software that was created in OpenDR H2020 research project based on this paper and the respective code provided by the authors. CelebA is a large scale facial dataset and consists of 202,599 facial images of 10,177 celebrities captured in the wild. The new dataset namely AUTH-OpenDR Augmented CelebA (AUTH-OpenDR ACelebA) was generated from 140,000 facial images corresponding to 9161 persons, i.e. a subset of CelebA was used. For each CelebA image used, 13 synthetic images generated by yaw axis camera rotation in the interval [0◦ : +60◦ ] with step +5◦ were obtained. Moreover, 10 synthetic images generated by pitch axis camera rotation in the interval [0◦: +45◦] with step +5◦ are also created for each facial image of the aforementioned dataset. Since CelebA license does not allow distribution of derivative work we do not make AcelebA directly available but instead provide instructions and scripts on how to recreate it.

- [AUTH-OpenDR Mixed Image Annotated Dataset for Human-centric Perception Tasks](https://zenodo.org/record/5801594#.Y-TgqhxBxhE)

The dataset was generated through a mixed (real and synthetic) image data generation method which utilizes real background images and DL-generated human models. It contains 50000 real images depicting urban scenes, populated by synthetic human models in various positions and poses and   is suitable for training/evaluating (a) pose estimation, (b) person detection, (c) identity recognition methods. Annotations for 2D bounding boxes of the depicted humans, their  IDs and 2D keypoints etc are provided. The 133 3D human models, required by the method, were generated using the Pixel-aligned Implicit Function (PIFu) and full-body images of people from the Clothing Co-Parsing (CCP) dataset. As background images, a subset of the Cityscapes dataset was used. The Cityscapes license prohibits the distribution of any modified versions of itself. Thus, we provide code  that can re-generate the exact same dataset, given that the Cityscapes dataset is downloaded by the website of its authors.

Code and instructions for re-generating the dataset are provided [here](https://github.com/opendr-eu/opendr/tree/master/projects/python/simulation/human_dataset_generation).

- [AUTH-OpenDR SMPL+D Human Bodies Dataset](https://zenodo.org/record/5801562#.Y-TgrBxBxhE)

The  dataset contains 2914 human bodies in various shapes and textures folowing the SMPL-D template. At its core, our dataset  consists of 183 unique SMPL+D bodies, which were generated through non-rigid shape registration of manually generated MakeHuman models. The rest were generated by applying shape and texture alterations to those models. In addition, we provide code for converting those human models in the FBX format.  However, pose-dependent deformations are not applied to the human models. Finally, instructions for setting a demo project in the Webots simulator are provided. In the project, one the SMPL+D models in FBX format can perform an animation from AMASS.

The dataset is available through the official GitHub repository of the OpenDR toolkit [here](https://github.com/opendr-eu/opendr/tree/master/projects/python/simulation/SMPL%2BD_human_models).
