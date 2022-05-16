<!--A curated list of resources for Image and Video Deblurring-->
<!-- PROJECT LOGO -->

<p align="center">
  <h2 align="center">Awesome-Image-Prior</h2>
  <p align="center">A curated list of resources for Prior in Image or Video 
    <br />
    <br />
    <br />
    <a href="https://github.com/yunfanLu/Awesome-Image-Prior/pulls/new">Suggest new item</a>
    <br />
    <a href="https://github.com/yunfanLu/Awesome-Image-Prior/issues/new">Report Bug</a>
  </p>
</p>



<h2>Table of contents</h2>

- [Image Enhancement Classification](#image-enhancement-classification)
- [Prior Classification](#prior-classification)
- [1.Ruled Prior](#1ruled-prior)
  - [1.1 High-Level Semantic Information as Prior](#11-high-level-semantic-information-as-prior)
  - [1.2 Image Statistical Features as Prior](#12-image-statistical-features-as-prior)
  - [1.3 Temporal Prior](#13-temporal-prior)
  - [1.4 Transformation as Prior](#14-transformation-as-prior)
  - [1.5 Physical-based Priors](#15-physical-based-priors)
  - [1.6 Explicit Modelling Kernel and Noise Information as Prior](#16-explicit-modelling-kernel-and-noise-information-as-prior)
  - [1.7 Data Degradation as Prior](#17-data-degradation-as-prior)
- [2. Latent Prior](#2-latent-prior)
  - [2.1 Non-local Self-similarity](#21-non-local-self-similarity)
  - [2.2 Facial Prior](#22-facial-prior)
  - [2.3 Deep Image Prior](#23-deep-image-prior)
  - [2.4 Pre-trained Model as Prior](#24-pre-trained-model-as-prior)

# Image Enhancement Classification

# Prior Classification


# 1.Ruled Prior

## 1.1 High-Level Semantic Information as Prior

**Definition:**

|Conference|Title|Task|
| ---- | :----------------------------------------------------------- | ---------- |
| TIP 2018 | Deep video dehazing with semantic segmentation              | Video Dehazing |
| CVPR 2018 | Deep semantic face deblurring | Human Face Deblur |
| CVPR 2018 | Recovering realistic texture in image super-resolution by deep spatial feature transform | Super-Resolution |
| CVPR 2018 | High-resolution image synthesis and semantic manipulation with conditional gans | Super-Resolution |
| CVPR 2019 | Human-aware motion deblurring | Human Motion Deblur |
| ICCV 2019 | Srobb: Targeted perceptual loss for single image superresolution | Super-Resolution |
| CVPR 2020 | Dual super-resolution learning for semantic segmentation | Super-Resolution |
| ACM-MM 2020 | Integrating semantic segmentation and retinex model for low-light image enhancement | Low-light; Denoise |
| CVPR 2021 | Progressive semantic-aware style transformation for blind face restoration | Human Face Restoration |
| ICCV 2021 | Spatiallyadaptive image restoration using distortion-guided networks | Image Restoration |
| ACM-MM 2022 | Close the loop: A unified bottomup and top-down paradigm for joint image deraining and segmentation | Deraining |
| WACV 2022 | Sapnet: Segmentation-aware progressive network for perceptual contrastive deraining | Deraining |

## 1.2 Image Statistical Features as Prior
Statistical image features can be divided into two categories, the statistical intensity features and the statistical gradient features.

<h2>Representative work</h2>

Representative application of statistical features in image/video restoration and enhancement tasks
|Publication|Title|Task|Statistical Features|Highlight|
|-|-|-|-|-|
[PAMI 2016](https://openreview.net/pdf?id=IucGD5fQBV)|L0 -regularized intensity and gradient prior for deblurring text images and beyond|Text deblurring|Two-tone distribution| $L_0$ regularization; Two-tone distribution 
[CVPR 2016](https://openaccess.thecvf.com/content_cvpr_2016/papers/Pan_Blind_Image_Deblurring_CVPR_2016_paper.pdf)|Blind image deblurring using dark channel prior| Deblurring| Dark channel| First work; Min operator linear approximation 
[CVPR 2017](https://openaccess.thecvf.com/content_cvpr_2017/papers/Yan_Image_Deblurring_via_CVPR_2017_paper.pdf)|Image deblurring via extreme channels prior| Deblurring| Bright channel| First work; Kernel estimation; Bright image 
ICIP 2017|Low-light image enhancement using CNN and bright channel prior| Low-light enhancement | Bright channel| As a part of the CNN model 
TIP 2017|Deep edge guided recurrent residual learning for image super-resolution| Super Resolution| Edge guided | First recurrent network model in SR  
CVPR 2019 | Blind image deblurring with local maximum gradient prior| Deblurring| Local maximum gradient prior  | First work; Local maximum gradient prior
AI 2019   | Single image dehazing using gradient channel prior| Dehazing| Gradient channel prior  | Gradient prior; Depth map 
ISPL 2020 |Unsupervised low-light image enhancement using bright channel prior| Low-light enhancement | Bright channel| Unsupervised learning approach 
CVPR 2020 | Structure-preserving super resolution with gradient guidance| Super Resolution| Gradient guidance | Proposed Gradient maps 

---

### 1.2.1 Statistical Intensity Features
Statistical features of high-quality image intensity have strong sparsity, which means the feature map or statistical values are mostly zeros. Their specific performance includes dark channel prior, bright channel prior, and two-tone distribution.

---
#### dark channels prior
[Deblurring] Blind image deblurring using dark channel prior, CVPR 2016.</br>
[Dehazing] Single image haze removal using dark channel prior, IEEE TPAMI 2010.</br>

#### bright channels prior
[Deblurring] Image deblurring via extreme channels prior, CVPR 2017.</br>
[Low-light] Low-light image enhancement using CNN and bright channel prior, ICPC 2017.</br>
[Low-light] Unsupervised low-light image enhancement using bright channel prior, IEEE Signal Processing Letters 2010.</br>

#### two-tone distribution
[Deblurring] L0 -regularized intensity and gradient prior for deblurring text images and beyond, TPAMI 2016.

#### two-color prior
[Deblurring&Denoising] Image deblurring and denoising using color priors, CVPR 2009.</br>

#### histogram equalization prior
[Survey] Histogram equalization variants as optimization problems: a review, Archives of Computational Methods in Engineering 2021. </br>
[Image-enhancement] Underwater image enhancement with global--local networks and compressed-histogram equalization, Signal Processing: Image Communication 2020.</br>

---

### 1.2.2 Statistical Gradient Feature
Statistical features of high-quality image intensity have strong sparsity, which means the feature map or statistical values are mostly zeros. Their specific performance includes dark channel prior, bright channel prior, and two-tone distribution.

---
#### local maximum gradient prior
[Deblurring] Blind image deblurring with local maximum gradient prior, CVPR 2019.
  
#### gradient guidance prior
[SR] Image super-resolution using gradient profile prior, CVPR 2008.</br>
[SR] Structure-preserving super resolution with gradient guidance, CVPR 2020.</br>

#### gradient channel prior
[Dehazing] Single image dehazing using gradient channel prior, Applied Intelligence 2019.</br>
[Dehazing] Color image dehazing using gradient channel prior and guided l0 filter, Information Sciences 2020.</br>

---


## 1.3 Temporal Prior
Temporal prior is specific in video restoration and enhancement tasks. Unlike the priors in the image, the priors in videos mainly come from temporal information, which is the relationship between frames.
### 1.3.1 Optical Flow
Optical flow is the motion of objects, surfaces, and edges between consecutive frames of sequence caused by the observer and scene.

<h2>Representative work</h2>

|Publication|Title|Task|Optical flow approach|Highlight|
|-|-|-|-|-|
|CVPR 2018|Frame-recurrent video super-resolution| VSR | FNet  |  Recurrent framework with optical flow estimation network(FNet)|
|IJCV 2019|Video enhancement with task-oriented flow| VSR | SPyNet| Task-oriented optical flow framework |
|NTIRE 2021|BasicVSR++: Improving video super-resolution with enhanced propagation and alignment| VSR | SPyNet | Use optical flow to guide the DCN|
|arXiv 2022|Vrt: A video restoration transformer| VSR | SPyNet | Use optical flow to guide the deep network based on self-attention |
|CVPR 2020|Cascaded deep video deblurring using temporal sharpness prior| Video deblurring | PWC-Net | Use optical flow to construct the temporal sharpness prior|
|CVPR 2021|Arvo: Learning all-range volumetric correspondence for video deblurring| Video deblurring | PWC-Net | Use optical flow to construct the temporal sharpness prior|
|CVPR 2021|Bringing events into video deblurring with non-consecutively blurry frames| Video deblurring | PWC-Net | Use optical flow to construct the temporal sharpness prior|
|CVPR 2019|Frame-consistent recurrent video deraining with dual-level flow| Video derainingR |FlowNet| Optical flow help extract the temporal rain-related feature|
|ICCP 2019|A fast, scalable, and reliable deghosting method for extreme exposure fusion| Multi-Exposure HDR |PWC-Net| Align multi-exposure image|
|TPAMI 2019|Memc-net: Motion estimation and motion compensation driven neural network for video interpolation and enhancement|video frame interpolation |PWC-net| Lead the flow-based motion interpolation algorithms| 

---
#### Deep learning-based optical methods
[Optical-flow] Flownet: Learning optical flow with convolutional networks, CVPR 2017.</br>
[Optical-flow] Flownet 2.0: Evolution of optical flow estimation with deep networks, CVPR 2017.</br>
[Optical-flow] Optical flow estimation using a spatial pyramid network, CVPR 2017.</br>
[Optical-flow] Pwc-net: Cnns for optical flow using pyramid, warping, and cost volume, CVPR 2018.</br>

---
#### Deep learning-based optical methods
![](img/optical-flow.png)

**(a)** Directly use optical flow in video super-resolution

[Video-super-resolution] Frame-recurrent video super-resolution, CVPR 2018.</br>
[Video-super-resolution] Video enhancement with task-oriented flow, IJCV 2019.</br>

**(b)** Combine DCN/attention with optical flow in video super-resolution

[Video-super-resolution] BasicVSR++: Improving video super-resolution with enhanced propagation and alignment, arXiv 2021.</br>
[Video-super-resolution] Vrt: A video restoration transformer. </br>

**(c)** Optical flow in multi-exposure HDR imaging

[Multi-Exposure-HDR] Deep high dynamic range imaging of dynamic scenes, ACM 2017.</br>
[Multi-Exposure-HDR] Multi-scale dense networks for deep high dynamic range imaging, WACV 2019.</br>
[Multi-Exposure-HDR] A fast, scalable, and reliable deghosting method for extreme exposure fusion, ICCP 2019.</br>
[Multi-Exposure-HDR] Deep HDR reconstruction of dynamic scenes, ICIVC 2018.</br>

**(d)** Construct temporal sharpness prior by optical flow

[Video-deblurring] Cascaded deep video deblurring using temporal sharpness prior, CVPR 2020.
[Video-deblurring] Bringing events into video deblurring with non-consecutively blurry frames, ICCV 2021.
[Video-deblurring] Arvo: Learning all-range volumetric correspondence for video deblurring, CVPR 2021.


**Others:**

### 1.3.2 Temporal Sharpness Prior

## 1.4 Transformation as Prior

### 1.4.1 Learning with Frequency Information

### 1.4.2 Other Transformation

## 1.5 Physical-based Priors

### 1.5.1 Atmospheric Scattering Model

### 1.5.2 Rain Model

### 1.5.3 Retinex Model

## 1.6 Explicit Modelling Kernel and Noise Information as Prior

### 1.6.1 Explicit Modelling in Modular Design

### 1.6.2 Explicit Modelling in Training Set Synthetic

## 1.7 Data Degradation as Prior

### 1.7.1 Motion Blur Model

### 1.7.2 Compression Information as Prior

# 2. Latent Prior

## 2.1 Non-local Self-similarity

## 2.2 Facial Prior

## 2.3 Deep Image Prior

## 2.4 Pre-trained Model as Prior

### 2.4.1 GAN Prior

### 2.4.2 Generative Priors in Training Set Synthetic

### 2.4.3 Deep Denoiser Prior for Regularization


