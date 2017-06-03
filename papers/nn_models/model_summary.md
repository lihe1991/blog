---
layout: default
---
# [](#header-1)Popular CNN Models

| Networks     | Layers| Top1 Error/Top5 Error| Size  | Year |
|:-------------|:------|:---------------------|:------|:-----|
| LeNet5       | 5     | 99.36 on MNIST       | 451KB | 1998 |
| [AlexNet](#alexnet)      | 8     | 40.7/18.2            | 240MB | 2012 |
| [VGG16](#vgg)        | 16    | 27/7.4               | 528MB | 2014 |
| [VGG19](#vgg)        | 19    | 27.3/7.3               | 548MB | 2014 |
| [GoogleLeNet](#googlenet)  | 22    | 22/6.67              | 96MB  | 2015 |
| [InceptionV1](#inception)  | 22    | 22/4.8             | 96MB  | 2015 |
| [InceptionV3](#inception)  | 22    | 21.2/5.6             | 96MB  | 2015 |
| ResNet-50    | 50    | 24.01/7.02           | 102MB | 2015 |
| ResNet-200   | 200   | 21.66/5.79           | 102MB | 2015 |

## [](#alexnet)AlexNet
**Review**([Paper link](http://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf))
This is an early work of using deep CNN. The tricky parts are the padding sizes and group sizes. Some groups sizes are set to 2 due to the memory limitation of GPU at that time. The model in Caffee Zoo also takes a group count of two.

**Bibtex**
```
@incollection{NIPS2012_4824,
title = {ImageNet Classification with Deep Convolutional Neural Networks},
author = {Alex Krizhevsky and Sutskever, Ilya and Hinton, Geoffrey E},
booktitle = {Advances in Neural Information Processing Systems 25},
editor = {F. Pereira and C. J. C. Burges and L. Bottou and K. Q. Weinberger},
pages = {1097--1105},
year = {2012},
publisher = {Curran Associates, Inc.},
url = {http://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf}
}
```
## [](#vgg)VGG
**Review**([Paper link](https://arxiv.org/pdf/1409.1556))
VggNet steadily increase the depth by adding more convolutional layers.
A lot of 3-by-3 convolutional filters are utilized.
Normally train with a decaying learning rate and around 70 epochs.

**Bibtex**
```
@article{DBLP:journals/corr/SimonyanZ14a,
  author    = {Karen Simonyan and
               Andrew Zisserman},
  title     = {Very Deep Convolutional Networks for Large-Scale Image Recognition},
  journal   = {CoRR},
  volume    = {abs/1409.1556},
  year      = {2014},
  url       = {http://arxiv.org/abs/1409.1556},
  timestamp = {Wed, 01 Oct 2014 15:00:05 +0200},
  biburl    = {http://dblp.uni-trier.de/rec/bib/journals/corr/SimonyanZ14a},
  bibsource = {dblp computer science bibliography, http://dblp.org}
}
}
```
## [](#googlenet)GoogLeNet
**Review**([Paper link](https://arxiv.org/pdf/1409.4842))
**Bibtex**
```
@article{DBLP:journals/corr/SzegedyLJSRAEVR14,
  author    = {Christian Szegedy and
               Wei Liu and
               Yangqing Jia and
               Pierre Sermanet and
               Scott E. Reed and
               Dragomir Anguelov and
               Dumitru Erhan and
               Vincent Vanhoucke and
               Andrew Rabinovich},
  title     = {Going Deeper with Convolutions},
  journal   = {CoRR},
  volume    = {abs/1409.4842},
  year      = {2014},
  url       = {http://arxiv.org/abs/1409.4842},
  timestamp = {Tue, 31 May 2016 18:15:20 +0200},
  biburl    = {http://dblp.uni-trier.de/rec/bib/journals/corr/SzegedyLJSRAEVR14},
  bibsource = {dblp computer science bibliography, http://dblp.org}
}
```
## [](#inception)Inception
**Review**([InceptionV1](https://arxiv.org/pdf/1502.03167), [InceptionV2,InceptionV3](https://arxiv.org/pdf/1512.00567))
In the Batch Norm paper, Sergey et al. proposed InceptionV1 architecture, which is very similar to GoogleNet.
They introduced the very important concept of batch norm to speed up learning and also increases accuracy.
Later on, the authors proposed InceptionV2 and InceptionV3.
In the Inception-v2, they introduced Factorization (factorize convolutions into smaller convolutions) and some minor change into Inception-v1.
As for Inception-v3, it is a variant of Inception-v2 which adds BN-auxiliary.


**Bibtex**
```
@article{DBLP:journals/corr/IoffeS15,
  author    = {Sergey Ioffe and
               Christian Szegedy},
  title     = {Batch Normalization: Accelerating Deep Network Training by Reducing
               Internal Covariate Shift},
  journal   = {CoRR},
  volume    = {abs/1502.03167},
  year      = {2015},
  url       = {http://arxiv.org/abs/1502.03167},
  timestamp = {Mon, 02 Mar 2015 14:17:34 +0100},
  biburl    = {http://dblp.uni-trier.de/rec/bib/journals/corr/IoffeS15},
  bibsource = {dblp computer science bibliography, http://dblp.org}
}

@article{DBLP:journals/corr/SzegedyVISW15,
  author    = {Christian Szegedy and
               Vincent Vanhoucke and
               Sergey Ioffe and
               Jonathon Shlens and
               Zbigniew Wojna},
  title     = {Rethinking the Inception Architecture for Computer Vision},
  journal   = {CoRR},
  volume    = {abs/1512.00567},
  year      = {2015},
  url       = {http://arxiv.org/abs/1512.00567},
  timestamp = {Sat, 02 Jan 2016 11:38:49 +0100},
  biburl    = {http://dblp.uni-trier.de/rec/bib/journals/corr/SzegedyVISW15},
  bibsource = {dblp computer science bibliography, http://dblp.org}
}
```
## [](#resnet)ResNet
**Review**([Paper link](https://arxiv.org/pdf/1512.03385))
**Bibtex**
```
@article{DBLP:journals/corr/HeZRS15,
  author    = {Kaiming He and
               Xiangyu Zhang and
               Shaoqing Ren and
               Jian Sun},
  title     = {Deep Residual Learning for Image Recognition},
  journal   = {CoRR},
  volume    = {abs/1512.03385},
  year      = {2015},
  url       = {http://arxiv.org/abs/1512.03385},
  timestamp = {Wed, 30 Mar 2016 23:40:00 +0200},
  biburl    = {http://dblp.uni-trier.de/rec/bib/journals/corr/HeZRS15},
  bibsource = {dblp computer science bibliography, http://dblp.org}
}
```

@inproceedings{deng2009imagenet,
  title={Imagenet: A large-scale hierarchical image database},
  author={Deng, Jia and Dong, Wei and Socher, Richard and Li, Li-Jia and Li, Kai and Fei-Fei, Li},
  booktitle={Computer Vision and Pattern Recognition, 2009. CVPR 2009. IEEE Conference on},
  pages={248--255},
  year={2009},
  organization={IEEE}
}



<!-- # [](#header-2)Citations
<a id='alexnet-paper'>
[1] Alex Krizhevsky, Ilya Sutskever, and Geoffrey E. Hinton. "ImageNet Classification with Deep Convolutional Neural Networks." NIPS 2012

<a id='inception-v1-paper'>
[2] Christian Szegedy, Wei Liu, Yangqing Jia, Pierre Sermanet, Scott Reed,
Dragomir Anguelov, Dumitru Erhan, Andrew Rabinovich.
"Going Deeper with Convolutions." CVPR 2015.

<a id='vgg-paper'>
[3] Karen Simonyan and Andrew Zisserman. "Very Deep Convolutional Networks for Large-Scale Image Recognition." ICLR 2015

<a id='resnet-cvpr'>
[4] Kaiming He, Xiangyu Zhang, Shaoqing Ren, and Jian Sun. "Deep Residual Learning for Image Recognition." CVPR 2016.

<a id='resnet-eccv'>
[5] Kaiming He, Xiangyu Zhang, Shaoqing Ren, and Jian Sun. "Identity Mappings in Deep Residual Networks." ECCV 2016. -->