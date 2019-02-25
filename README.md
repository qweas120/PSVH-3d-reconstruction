# PSVH-3d-reconstruction
This repository is the implementation of our AAAI 2019 paper:

[Deep Single-View 3D Object Reconstruction with Visual Hull Embedding](https://arxiv.org/pdf/1809.03451.pdf)

[Hanqing Wang](https://qweas120.github.io), [Jiaolong Yang](http://jlyang.org/), [Wei Liang](http://iitlab.bit.edu.cn/mcislab/~liangwei/), [Xin Tong](http://www.xtong.info/)

This work is implemented using [TensorFlow](https://www.tensorflow.org/).
## Introduction
In this paper, we present an approach which aims to preserve more shape details and improve the reconstruction quality. The key idea of our method is to leverage object mask and pose estimation from CNNs to assist the 3D shape learning by constructing a probabilistic single-view visual hull inside of the network. 

<img src="./readme/img/network.png">

Our method works by first predicting a coarse shape as well as the object pose and silhouette using CNNs, followed by a novel 3D refinement CNN which refines the coarse shapes using the constructed probabilistic visual hulls.
<!-- ![image](./readme/img/results/result.png) -->
<!-- <img src="./readme/img/results/result.png" align="center" width="65%"> -->

## Examples
<img src="./readme/img/results/result.png" align="center" width="100%">

## Citation
If you find our work helpful for your research, please cite our paper:
```
@article{wang2018deep,
  title={Deep Single-View 3D Object Reconstruction with Visual Hull Embedding},
  author={Wang, Hanqing and Yang, Jiaolong and Liang, Wei and Tong, Xin},
  journal={arXiv preprint arXiv:1809.03451},
  year={2018}
}

```
## Installation
Install python and the dependencies:
- python `3.5`
- tensorflow `1.12.0`
- pillow

If your python environments are managed via Anaconda/Miniconda, you can install the dependencies using the following scrpit:
``` shell
conda install tensorflow pillow
```
The checkpoint of the trained models are available [here](https://drive.google.com/open?id=1TJEUUhmZL8WJgQbsrRX9D_GKAiqE8Gic)(426MB). Extract the files to the root directory.

## Demo

Run `python run_case.py` to run the examples. The outputs are reconstruction results before and after the refinement (Please refer to our paper for more details). The results are in `obj` format. You can use [meshlab](http://www.meshlab.net/) for visulization.    

## Acknowlegement



## License
PSVH is freely available for non-commercial use, and may be redistributed under these conditions. Please see the license for further details. For commercial license, please contact the authors.