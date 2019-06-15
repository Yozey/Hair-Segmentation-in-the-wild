## Human Hair Segmentation In The Wild Using Deep Shape Prior
[**Yongzhe Yan**](mailto:yongzhe.yan@etu.uca.fr)<sup>1,2</sup> , [Anthony Berthelier](mailto:anthony.berthelier@etu.uca.fr)<sup>1,2</sup> , [Stefan Duffner](mailto:stefan.duffner@liris.cnrs.fr)<sup>3</sup> , Xavier Naturel <sup>2</sup> , [Christophe Garcia](mailto:christophe.garcia@liris.cnrs.fr) <sup>3</sup> , [Thierry Chateau](mailto:thierry.chateau@uca.fr) <sup>1</sup> <br>
<sup>1</sup>Université Clermont Auvergne     <sup>2</sup>Wisimage      <sup>3</sup>LIRIS <br>
Presented at the Third Workshop on CV4ARVR, CVPR 2019, Long Beach <br>


### Abstract

Virtual human hair dying is becoming a popular Augmented Reality (AR) application in recent years. Human hair contains diverse color and texture information which can be significantly varied from case to case depending on different hair styles and environmental lighting conditions. However, the publicly available hair segmentation datasets are relatively small. As a result, hair segmentation can be easily interfered by the cluttered background in practical use. In this paper, we propose to integrate a shape prior into Fully Convolutional Neural Network (FCNN) to mitigate this issue. First, we utilize a FCNN with an Atrous Spatial Pyramid Pooling (ASPP) module [1] to find a human hair shape prior based on a specific distance transform. In the second stage, we combine the hair shape prior and the original image to form the input of a symmetric encoder-decoder FCNN to get the final hair segmentation output. Both quantitative and qualitative results show that our method achieves state-of-the-art performance on the publicly available LFW-Part and Figaro1k datasets.

### Challenge
* **Human Hair Segmentation In The Wild:** Perform hair segmentation in an unconstrained view without any explicit prior face/head-shoulder detection.
* **A problem in practical application:** Cluttered Background disturbs deep CNN segmentation especially when the dataset is small, which brings spurious detections.

![Spurious Detection](/Spurious.png)

### Our Structure
* We propose to construct a **shape prior** to constrain and guide the hair segmentation.

![Structure](/CVPRW_overall.svg)
