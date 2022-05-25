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

# 1.Ruled Prior

## 1.1 High-Level Semantic Information as Prior
The high-level information refers to using semantic segmentation or object detection information as priors to guide image restoration and enhancement.

<h2>Representative work</h2>

|Publication|Title|Task|Statistical Prior|Highlight|
|-|-|-|-|-|
|[TIP 2018](https://ieeexplore.ieee.org/abstract/document/8492451?casa_token=uv8Cdpbgn4wAAAAA:aAyXn6-5v7orDxILciKbgBJKz6nQSPzMwF-z1Ptgh-ndm8i4INcpzqftgbdfaG4B87wc6ySadg)|Deep video dehazing with semantic segmentation| Video Dehazing    | Semantic  | Video     
|[CVPR 2018](https://openaccess.thecvf.com/content_cvpr_2018/html/Shen_Deep_Semantic_Face_CVPR_2018_paper.html)|Deep semantic face deblurring| Face deblur| Semantic  | Perceptual and adversarial losses 
|CVPR 2018|Fsrnet: End-to-end learning face super-resolution with facial priors| Face Super-Resolution     | Face landmark     | First work, Face landmark heatmaps 
|CVPR 2018|Recovering realistic texture in image super-resolution by deep spatial feature transform| Super-Resolution  | Semantic  | Textures recover 
|CVPR 2018|High-resolution image synthesis and semantic manipulation with conditional gans| Super Resolution  | Semantic  | GAN-based 
|CVPR 2019|Human-aware motion deblurring| Human Motion Deblur| Semantic  | Disentangles the humans and background 
|ICCV 2019|Srobb: Targeted perceptual loss for single image super-resolution| Super resolution  | Semantic  | Object, Background and Boundary 
|CVPR 2020|Dual super-resolution learning for semantic segmentation| Super-Resolution  | Semantic  | Two-stream framework   
|ACM-MM 2020     |Integrating semantic segmentation and retinex model for low-light image enhancement| Low-light; Denoise| Semantic  | First work 
|TIP 2020|Connecting image denoising and high-level vision tasks via deep learning| Denoise   | Semantic  | First work  
|CVPR 2021|Progressive semantic-aware style transformation for blind face restoration| Human face restoration    | Semantic  | Semantic-aware style Transformation 
|ICCV 2021|Spatially-adaptive image restoration using distortion-guided networks| Image Restoration | Semantic  | *
|ACM-MM 2022 |Close the Loop: A Unified Bottom-up and Top-down Paradigm for Joint Image Deraining and Segmentation| Deraining | Semantic  | Bottom-up and Top-down Paradigm 

---

![](img/14-high-level-guide.jpg)

**(a)** the semantic output as the input for the image restoration and enhancement model. 

- [Face-restoration] Towards real-world blind face restoration with generative facial prior, CVPR 2021.
- [Face-deblurring] Deep semantic face deblurring, CVPR 2018.

**(b)** the restoration and enhancement and the semantic model shell one backbone and training together. 

- [Denoising] Connecting image denoising and high-level vision tasks via deep learning, TIP 2020.

**(c)** enhancement and segmentation tasks are alternatively performed and collaborated with each other

- [Deraining] Close the Loop: A Unified Bottom-up and Top-down Paradigm for Joint Image Deraining and Segmentation, 2022.

---

- [Survey] Deep semantic segmentation of natural and medical images: a review, Artificial Intelligence Review 2021.
- [Survey] Deep learning for generic object detection: A survey, IJCV 2020.
- [Face-restoration] Learning warped guidance for blind face restoration, ECCV 2018.

## 1.2 Image Statistical Features as Prior
Statistical image features can be divided into two categories, the statistical intensity features and the statistical gradient features.

<h2>Representative work</h2>

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

#### dark channels prior
- [Deblurring] Blind image deblurring using dark channel prior, CVPR 2016.
- [Dehazing] Single image haze removal using dark channel prior, IEEE TPAMI 2010.

#### bright channels prior
- [Deblurring] Image deblurring via extreme channels prior, CVPR 2017.
- [Low-light] Low-light image enhancement using CNN and bright channel prior, ICPC 2017.
- [Low-light] Unsupervised low-light image enhancement using bright channel prior, IEEE Signal Processing Letters 2010.

#### two-tone distribution
- [Deblurring] L0 -regularized intensity and gradient prior for deblurring text images and beyond, TPAMI 2016.

#### two-color prior
- [Deblurring&Denoising] Image deblurring and denoising using color priors, CVPR 2009.

#### histogram equalization prior
- [Survey] Histogram equalization variants as optimization problems: a review, Archives of Computational Methods in Engineering 2021. 
- [Image-enhancement] Underwater image enhancement with global--local networks and compressed-histogram equalization, Signal Processing: Image Communication 2020.

---

### 1.2.2 Statistical Gradient Feature
Statistical features of high-quality image intensity have strong sparsity, which means the feature map or statistical values are mostly zeros. Their specific performance includes dark channel prior, bright channel prior, and two-tone distribution.

#### local maximum gradient prior
- [Deblurring] Blind image deblurring with local maximum gradient prior, CVPR 2019.
  
#### gradient guidance prior
- [Super-resolution] Image super-resolution using gradient profile prior, CVPR 2008.
- [Super-resolution] Structure-preserving super resolution with gradient guidance, CVPR 2020.

#### gradient channel prior
- [Dehazing] Single image dehazing using gradient channel prior, Applied Intelligence 2019.
- [Dehazing] Color image dehazing using gradient channel prior and guided l0 filter, Information Sciences 2020.

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
- [Optical-flow] Flownet: Learning optical flow with convolutional networks, CVPR 2017.
- [Optical-flow] Flownet 2.0: Evolution of optical flow estimation with deep networks, CVPR 2017.
- [Optical-flow] Optical flow estimation using a spatial pyramid network, CVPR 2017.
- [Optical-flow] Pwc-net: Cnns for optical flow using pyramid, warping, and cost volume, CVPR 2018.

---
#### Deep learning-based optical methods
![](img/optical-flow.png)

**(a)** Directly use optical flow in video super-resolution

- [VSR] Frame-recurrent video super-resolution, CVPR 2018.
- [VSR] Video enhancement with task-oriented flow, IJCV 2019.

**(b)** Combine DCN/attention with optical flow in video super-resolution

- [VSR] BasicVSR++: Improving video super-resolution with enhanced propagation and alignment, arXiv 2021.
- [VSR] Vrt: A video restoration transformer. 

*VSR without optical flow:
- [VSR] Deep video super-resolution network using dynamic upsampling filters without explicit motion compensation, CVPR 2018.
- [VSR] Edvr: Video restoration with enhanced deformable convolutional networks, CVPR Workshops 2019.
- [VSR] Tdan: Temporally-deformable alignment network for video super-resolution, CVPR 2020.

**(c)** Optical flow in multi-exposure HDR imaging

- [Multi-Exposure-HDR] Deep high dynamic range imaging of dynamic scenes, ACM 2017.
- [Multi-Exposure-HDR] Multi-scale dense networks for deep high dynamic range imaging, WACV 2019.
- [Multi-Exposure-HDR] A fast, scalable, and reliable deghosting method for extreme exposure fusion, ICCP 2019.
- [Multi-Exposure-HDR] Deep HDR reconstruction of dynamic scenes, ICIVC 2018.

**(d)** Construct temporal sharpness prior by optical flow

- [Video-deblurring] Cascaded deep video deblurring using temporal sharpness prior, CVPR 2020.
- [Video-deblurring] Bringing events into video deblurring with non-consecutively blurry frames, ICCV 2021.
- [Video-deblurring] Arvo: Learning all-range volumetric correspondence for video deblurring, CVPR 2021.


**Others:**
- [Optical-flow] Large displacement optical flow: descriptor matching in variational motion estimation, TPAMI 2010.
- [Video-deraining] Frame-consistent recurrent video deraining with dual-level flow, CVPR 2019.
- [Video-frame-interpolation] Memc-net: Motion estimation and motion compensation driven neural network for video interpolation and enhancement, TPAMI 2019.

### 1.3.2 Temporal Sharpness Prior
Temporal sharpness prior is a specific prior in video deblurring based on the hypothesis of blur inconsecutive property.

- [Video-deblurring] Video deblurring for hand-held cameras using patch-based synthesis, ACM TOG 2012.
- [Video-deblurring] Cascaded deep video deblurring using temporal sharpness prior, CVPR 2020.
- [Video-deblurring] Bringing events into video deblurring with non-consecutively blurry frames, ICCV 2021.
- [Video-deblurring] Arvo: Learning all-range volumetric correspondence for video deblurring, CVPR 2021.

## 1.4 Transformation as Prior
Transforming image to different domain can bring favorable properties for network training e.g., some noise pattern are more apparent in certain frequency sub-bands.

<h2>Representative work</h2>

|Publication|Title|Task|Transformation Types|Highlight|
|-|-|-|-|-|
CVPRW 2017 | Beyond deep residual learning for image restoration: Persistent homology-guided manifold simplification | SR</br>Denoising | Wavelet | Use as input and output in CNN |
CVPRW 2017 | Deep wavelet prediction for image super-resolution | SR | Wavelet | Use as input and output in CNN |
CVPRW 2018 | Multi-level wavelet-CNN for image restoration | SR</br>Denoising</br>Compression| Wavelet | Apply on feature map in CNN |
ICCV 2017 | Wavelet-srnet: A wavelet-based cnn for multi-scale face super resolution | SR | Wavelet | Use as input and output in CNN|
TIP 2019 | Scale-free single image deraining via visibility-enhanced recurrent wavelet learning | Deraning | Wavelet | Use as input and output in CNN|
ICCV 2019 | Wavelet domain style transfer for an effective perception-distortion tradeoff in single image super-resolution | SR | Wavelet | Use as input and output in CNN |
ECCV 2020 | Wavelet-based dual-branch network for image demoiring | Demoireing</br>Deraining | Wavelet | Use input and output in CNN |
ECCV 2020 | Burst Denoising via Temporally Shifted Wavelet Transforms | Denoising | Wavelet | Apply on feature map in CNN |
CVPRW 2021 | DW-GAN: A Discrete Wavelet Transform GAN for NonHomogeneous Dehazing | Dehazing | Wavelet | Apply on feature map in GAN |
CVPR 2021 | Invertible denoising network: A light solution for real noise removal | Denoising | Wavelet | Use as input and output in invertible network|
CVPR 2021 | Efficient multi-stage video denoising with recurrent spatio-temporal fusion | Denoising | Customized Wavelet | Use as input and output in CNN |
ICCV 2021 | Fourier space losses for efficient perceptual image super-resolution | SR | Fourier | Use as input and output in GAN |
ICCV 2021 | ALL Snow Removed: Single Image Desnowing Algorithm Using Hierarchical Dual-Tree Complex Wavelet Representation and Contradict Channel Loss | Desnowing | Wavelet | Use as input and output in CNN |

---
### 1.4.1 Learning with Frequency Information
Transforming data into the frequency domain, such as using Discrete Fourier Transform (DFT) or Discrete Wavelet Transform (DWT), allows data to be decomposed with different frequency sub-bans for component-wise analysis, and has been widely studied for image restoration before deep learning era.

- [Theory] A theory for multiresolution signal decomposition: the wavelet representation, TPAMI 1989.
- [Image-restoration] An EM algorithm for wavelet-based image restoration, TIP 2003.
- [Image-restoration] Beyond deep residual learning for image restoration: Persistent homology-guided manifold simplification, CVPRW 2017.
- [Demoiring] Wavelet-based dual-branch network for image demoiring, ECCV 2020.
- [Deraining] Scale-free single image deraining via visibility-enhanced recurrent wavelet learning, TIP 2019.
- [Dehazing] DW-GAN: A Discrete Wavelet Transform GAN for NonHomogeneous Dehazing, CVPRW 2021.
- [Desnowing] ALL Snow Removed: Single Image Desnowing Algorithm Using Hierarchical Dual-Tree Complex Wavelet Representation and Contradict Channel Loss, ICCV 2021.
- [Super-resolution] Deep wavelet prediction for image super-resolution, CVPRW 2017.
- [Super-resolution] Wavelet-srnet: A wavelet-based cnn for multi-scale face super resolution, ICCV 2017.
- [Super-resolution] Wavelet domain style transfer for an effective perception-distortion tradeoff in single image super-resolution, ICCV 2019.
- [Denoising] Invertible denoising network: A light solution for real noise removal, CVPR 2021.
- [Denoising] Efficient multi-stage video denoising with recurrent spatio-temporal fusion, CVPR 2021.
- [Super-resolution] Fourier space losses for efficient perceptual image super-resolution, ICCV 2021.
- [Image-restoration] Multi-level wavelet-CNN for image restoration, CVPRW 2018.
- [Denoising] Burst Denoising via Temporally Shifted Wavelet Transforms, ECCV 2020.

### 1.4.2 Other Transformation
There are also other transformations that can serve as informative prior for image restoration and enhancement tasks by emphasizing some significant patterns of images.

- [Super-resolution] Deep edge guided recurrent residual learning for image super-resolution, TIP 2017.
- [Super-resolution] Edge-informed single image super-resolution, ICCVW 2019. 
- [Dehazing] Single image dehazing via multi-scale convolutional neural networks with holistic edges, IJCV 2020.
- [Low-light] Eemefn: Low-light image enhancement via edge-enhanced multi-exposure fusion network, AAAI 2020.
- [Edge-detection] Holistically-nested edge detection, ICCV 2015.
- [Super-resolution] Soft-edge assisted network for single image super-resolution, TIP 2020.
- [Dehazing] Gated fusion network for single image dehazing, CVPR 2018.



## 1.5 Physical-based Priors
Physical model can simplify the learning target compared to the directly output high-quality image.

<h2>Representative work</h2>

|Publication|Title|Task|Physical Prior|Highlight|
|-|-|-|-|-|
TIP 2016 | Dehazenet: An end-to-end system for single image haze removal | Dehazing | ASM | Estimate transmission map|
ECCV 2016 | Single image dehazing via multi-scale convolutional neural networks  | Dehazing | ASM | Estimate transmission map |
ICCV 2017 | Aod-net: All-in-one dehazing network | Dehazing | ASM | Estimate an intermediate parameter by reformulated ASM |
CVPR 2018 | Densely connected pyramid dehazing network| Dehazing | ASM | Jointly estimate transmission map and atmospheric light|
IJCAI 2018 | DehazeGAN: When Image Dehazing Meets Differential Programming. | Dehazing | ASM | Estimate an intermediate parameter by reformulated ASM |
TIP 2019 | FAMED-Net: A fast and accurate multi-scale end-to-end dehazing network | Dehazing | ASM | Estimate an intermediate parameter by reformulated ASM |
ECCV 2020 | Physics-based feature dehazing networks | Dehazing | ASM | Jointly estimate transmission map and atmospheric light|
ECCV 2020 | BidNet: Binocular image dehazing without explicit disparity estimation | Dehazing | ASM | Jointly estimate transmission map and atmospheric light|
ECCV 2020 | JSTASR: Joint size and transparency-aware snow removal algorithm based on modified partial convolution and veiling effect removal | Desnowing | ASM | Jointly estimate transmission map and atmospheric light |
CVPR 2021 | Zero-Shot Single Image Restoration Through Controlled Perturbation of Koschmieder's Model | Dehazing</br>Underwater</br>Low-light | ASM |  Jointly estimate transmission map and atmospheric light |
CVPR 2017 | Removing rain from single images via a deep detail network | Deraining | Rain Model | Residual learning |
CVPR 2017 | Deep edge guided recurrent residual learning for image super-resolution  | Deraining | Rain Model | Recurrent Residual learning with multiple steak layer and rain mask|
CVPR 2018 | Density-aware single image de-raining using a multi-stream dense network | Deraining | Rain Model | Residual learning with rain-density classifier|
ECCV 2018 | Recurrent squeeze-and-excitation context aggregation net for single image deraining | Deraining | Rain Model | Recurrent Residual learning with multiple steak layer|
CVPR 2018 | Erase or fill? deep joint recurrent rain removal and reconstruction in videos  | Video Deraining | Rain Model | Residual learning considering occlusion|
CVPR 2019 | Depth-attentional features for single-image rain removal | Deraining | Rain Model | Residual learning with depth information guidance |
CVPR 2019 | Frame-consistent recurrent video deraining with dual-level flow  | Video Deraining | Rain Model | Residual learning with temporal fusion |
BMVC 2018 | Deep Retinex Decomposition for Low-Light Enhancement |  Low-light | Retinex Model | Estimate reflectance and illumination |
PRL 2018 | LightenNet: A convolutional neural network for weakly illuminated image enhancement |  Low-light | Retinex Model | Estimate illumination|
ACM MM 2019 | Kindling the darkness: A practical low-light image enhancer |  Low-light | Retinex Model | Estimate reflectance and illumination |
ACM MM 2019 | Progressive retinex: Mutually reinforced illumination-noise perception network for low-light image enhancement |  Low-light | Retinex Model | Estimate illumination |
IJCV 2021 | Beyond brightening low-light images |  Low-light | Retinex Model | Estimate reflectance and illumination |
TIP 2021 | Sparse gradient regularized deep retinex network for robust low-light image enhancement |  Low-light | Retinex Model | Estimate reflectance and illumination|
CVPR 2021 | Retinex-inspired unrolling with cooperative prior architecture search for low-light image enhancement |  Low-light | Retinex Model | Estimate illumination|

### 1.5.1 Atmospheric Scattering Model
- [Theory] Vision in bad weather, ICCV 1999.
- [Theory] Contrast restoration of weather degraded images, TPAMI 2003.
- [Dehazing] Dehazenet: An end-to-end system for single image haze removal, TIP 2016.
- [Dehazing] Densely connected pyramid dehazing network, CVPR 2018.
- [Dehazing] Aod-net: All-in-one dehazing network, ICCV 2017.
- [Dehazing] DehazeGAN: When Image Dehazing Meets Differential Programming., IJCAI 2018.
- [Dehazing] FAMED-Net: A fast and accurate multi-scale end-to-end dehazing network, TIP 2019.
- [Dehazing] Physics-based feature dehazing networks, ECCV 2020.
- [Desnowing] JSTASR: Joint size and transparency-aware snow removal algorithm based on modified partial convolution and veiling effect removal, ECCV 2020.
- [Restoration] Zero-Shot Single Image Restoration Through Controlled Perturbation of Koschmieder's Model, CVPR 2021.

### 1.5.2 Rain Model
- [Deraining] Rain streak removal using layer priors, CVPR 2016.
- [Deraining] Removing rain from single images via a deep detail network, CVPR 2017.
- [Deraining] Density-aware single image de-raining using a multi-stream dense network, CVPR 2018.
- [Super-resolution] Deep edge guided recurrent residual learning for image super-resolution, TIP 2017.
- [Deraining] Erase or fill? deep joint recurrent rain removal and reconstruction in videos, CVPR 2018.
- [Deraining] Frame-consistent recurrent video deraining with dual-level flow, CVPR 2019.
- [Deraining] Depth-attentional features for single-image rain removal, CVPR 2019.

### 1.5.3 Retinex Model
- [Theory] An alternative technique for the computation of the designator in the retinex theory of color vision,1986.
- [Low-Light] Deep Retinex Decomposition for Low-Light Enhancement, BMVC 2018.
- [Low-Light] Kindling the darkness: A practical low-light image enhancer, ACM-MM 2019.
- [Low-Light] Beyond brightening low-light images, IJCV 2021.
- [Low-Light] Sparse gradient regularized deep retinex network for robust low-light image enhancement, TIP 2021.
- [Low-Light] LightenNet: A convolutional neural network for weakly illuminated image enhancement, Pattern recognition letters 2018.
- [Low-Light] Progressive retinex: Mutually reinforced illumination-noise perception network for low-light image enhancement, ACM-MM 2019.
- [Low-Light] Retinex-inspired unrolling with cooperative prior architecture search for low-light image enhancement, CVPR 2021.

## 1.6 Explicit Modelling Kernel and Noise Information as Prior
Modeling kernel and noise information can provide extra information and perform image-specific restoration.

<h2>Representative work</h2>

|Publication|Title|Task|Highlight|
|-|-|-|-|
|CVPR 2018 | Learning a single convolutional super-resolution network for multiple degradations  | SR | Kernel for conditional input |
|TIP 2018 | FFDNet: Toward a fast and flexible solution for CNN-based image denoising  | Denoising | Noise for conditional input |
|CVPR 2019| Deep plug-and-play super-resolution for arbitrary blur kernels  | SR | Kernel for conditional input |
|NeurIPS 2019 | Blind super-resolution kernel estimation using an internal-gan | SR | Estimate kernel |
|CVPR 2019 | Blind super-resolution with iterative kernel correction  | SR | Jointly estimate and conditional</br>input kernel information|
|CVPR 2019 | Toward convolutional blind denoising of real photographs  | Denoising | Jointly estimate and conditional </br> input noise information |
|CVPR 2020 | Unified dynamic convolutional network for super-resolution with variational degradations | SR |  Kernel for conditional input |
|NeurIPS 2020 | Unfolding the alternating optimization for blind super resolution  | SR | Jointly estimate and conditional </br> input kernel information |
|CVPR 2021 | Flow-based kernel prior with application to blind super-resolution  | SR |  Estimate kernel |
|CVPR 2018 | Image blind denoising with generative adversarial network based noise modeling | Denoising | Synthetic noise modeling |
|ICCV 2019 | Kernel modeling super-resolution on real low-resolution images  | SR | Synthetic kernel modeling   |
|CVPRW 2020 |Real-world super-resolution via kernel estimation and noise injection | SR | Synthetic kernel modeling |
|CVPR 2021 | Explore image deblurring via encoded blur kernel space  | Deblur |  Synthetic kernel modeling  |
|ICCV 2021 | C2N: Practical Generative Noise Modeling for Real-World Denoising | Denoising | Synthetic noise modeling |

### 1.6.1 Explicit Modelling in Modular Design
- [Super-resolution] Learning a single convolutional super-resolution network for multiple degradations, CVPR 2018.
- [Super-resolution] Unified dynamic convolutional network for super-resolution with variational degradations, CVPR 2020.
- [Super-resolution] Deep plug-and-play super-resolution for arbitrary blur kernels, CVPR 2019.
- [Super-resolution] Neural blind deconvolution using deep priors, CVPR 2020.
- [Super-resolution] Learning the Non-differentiable Optimization for Blind Super-Resolution, CVPR 2021.
- [Denoising] FFDNet: Toward a fast and flexible solution for CNN-based image denoising, TIP 2018.
- [Super-resolution] Blind super-resolution kernel estimation using an internal-gan, NIPS 2019.
- [Super-resolution] Flow-based kernel prior with application to blind super-resolution, CVPR 2021.
- [Super-resolution] Blind super-resolution with iterative kernel correction, CVPR 2019.
- [Super-resolution] Unfolding the alternating optimization for blind super resolution, NIPS 2020.
- [Denoising] Toward convolutional blind denoising of real photographs, CVPR 2019.

### 1.6.2 Explicit Modelling in Training Set Synthetic
- [Super-resolution] Kernel modeling super-resolution on real low-resolution images, ICCV 2019.
- [Super-resolution] Real-world super-resolution via kernel estimation and noise injection, CVPRW 2020.
- [Deblurring] Explore image deblurring via encoded blur kernel space, CVPR 2021.
- [Denoising] Image blind denoising with generative adversarial network based noise modeling, CVPR 2018.
- [Denoising] C2N: Practical Generative Noise Modeling for Real-World Denoising, ICCV 2021.
- [Super-resolution] Unsupervised degradation representation learning for blind super-resolution, CVPR 2021.
- [Super-resolution] Classsr: A general framework to accelerate super-resolution networks by data characteristic, CVPR 2021.

## 1.7 Data Degradation as Prior
### 1.7.1 Motion Blur Model
- [Deblurring] Deep multi-scale convolutional neural network for dynamic scene deblurring, CVPR 2017.
- [VSR&Video-deblurring] Ntire 2019 challenge on video deblurring and super-resolution: Dataset and study, CVPRW 2019.
- [Deblurring] NTIRE 2021 challenge on image deblurring, CVPR 2021.
- [Slow-motion] Deep slow motion video reconstruction with hybrid imaging system, TPAMI 2020.

### 1.7.2 Compression Information as Prior
- [Compression] Characterizing perceptual artifacts in compressed video streams,Human Vision and Electronic Imaging XIX 2014.
- [Compression] Deep kalman filtering network for video compression artifact reduction, ECCV 2018.
- [Compression] Enhancing quality for HEVC compressed videos, IEEE Transactions on Circuits and Systems for Video Technology 2018.
- [Compression] Non-local convlstm for video compression artifact reduction, ICCV 2019.
- [Super-resolution] Real-esrgan: Training real-world blind super-resolution with pure synthetic data, ICCV 2021.
- [VSR] Video enhancement with task-oriented flow, IJCV 2019.
- [Compression] NTIRE 2021 challenge on quality enhancement of compressed video: Methods and results, CVPR 2021.

# 2. Latent Prior

## 2.1 Non-local Self-similarity
Non-local self-similarity prior can help restore and enhance specific details with the reappearance patches in an image.

- [Denoising] Image denoising by sparse 3-D transform-domain collaborative filtering, TIP 2007.
- [Denoising] Weighted nuclear norm minimization with application to image denoising, CVPR 2014.
- [Super-resolution] Image super-resolution with cross-scale non-local attention and exhaustive self-exemplars mining, CVPR 2020.
- [Super-resolution] Image super-resolution with non-local sparse attention, CVPR 2021.
- [Restoration] Residual non-local attention networks for image restoration, arXiv 2019.
- [Restoration] Image restoration via simultaneous nonlocal self-similarity priors, TIP 2020.
- [Restoration] Non-local recurrent network for image restoration, NIPS 2018.
- [Theory] Non-local neural networks, CVPR 2018.
- [Super-resolution] Second-order attention network for single image super-resolution, CVPR 2019.

## 2.2 Facial Prior
Features such as the unique geometry and structure of the face and facial components can be utilized to solve deep learning-based facial image enhancement and restoration tasks.

<h2>Representative work</h2>

|Publication|Title|Task|prior|Highlight|
|-|-|-|-|-|
ECCV 2018|Learning warped guidance for blind face restoration|Face Restoration|Reference-based Prior |High-quality guided image of the same identity    | 
ECCV 2018|Face super-resolution guided by facial component heatmaps|Face SR  |Facial Component      |Facial component heatmaps| 
CVPR 2018|Fsrnet: End-to-end learning face super-resolution with facial priors|Face Hallucination (SR)|Geometry|Facial Landmarks / Parsing Maps  | 
CVPR 2018|Super-fan: Integrated facial landmark localization and super-resolution of real-world low resolution faces in arbitrary poses with gans|Face Hallucination (SR)|Geometry|End-to-end face SR and landmark localization  | 
IJCV 2019|Motion deblurring of faces|Face Deblur     &Geometry |Facial Landmarks / Parsing Maps  | 
BMVC2019 |Progressive face super-resolution via attention to facial landmark |Face Hallucination (SR)|Geometry|Facial Landmarks| 
ECCV 2020|Blind face restoration via deep multi-scale component dictionaries|Face Restoration|Reference-based Prior |Deep face components dictionaries  | 
CVPR 2020|Deep face super-resolution with iterative collaboration between attentive recovery and landmark estimation|Face Hallucination (SR)|Geometry|Facial Landmarks / Parsing Maps  | 
CVPR 2020|Enhanced blind face restoration with multi-exemplar images and adaptive spatial feature fusio |Face Hallucination (SR)|Reference-based Prior |High quality images as reference | 
WACV 2020|Component attention guided face super-resolution network: Cagface |Face Hallucination (SR)|Facial Component      |Facial component-wise attention maps     | 
IJCV 2020|FPN \|Exploiting semantics for face image deblurring |Face Deblur     |Facial Component      |Semantic labels priors and local structures prior | 
TIP 2020 |Deblurring face images using uncertainty guided multi-stream semantic networks |Face Deblur     |Facial Component      |Semantic labels priors  | 
TIP 2020 |Face hallucination using cascaded super-resolution and identity priors |Face Hallucination (SR)|Recognition Model     |Identity priors from face recognition models    | 
ICIP 2021|2021 IEEE International Conference on Image Processing (ICIP) |Face Hallucination (SR)|Facial Component      |Non-parametric facial prior     | 
NeurIPS 2021    |Progressive semantic-aware style transformation for blind face restoration |Face Restoration|Parsing Maps   |Semantic aware style transformation     | 
TPAMI 2021      |Face Restoration via Plug-and-Play 3D Facial Priors  |Face Restoration|Geometry|Plug-and-play 3D facial priors | 
CVPR 2021|Progressive semantic-aware style transformation for blind face restoration |Face Restoration|Geometry|Parsing Maps  | 
CVPR 2021|Towards real-world blind face restoration with generative facial prior|Face Restoration|GAN Facial Prior      |Prior in a pretrained face GAN  | 
CVPR 2021|GAN prior embedded network for blind face restoration in the wild |Face Restoration|GAN Facial Prior      |Fine-tune the GAN prior embedded DNN  | 
WACV 2022|Deep Feature Prior Guided Face Deblurring  |Face Deblur     |Recognition Model     |Deep features of face recognition networks  

## 2.3 Deep Image Prior
- [Restoration] Deep Image Prior, IJCV 2020.
- [Theory] Deep decoder: Concise image representations from untrained non-convolutional networks?, arXiv 2018.
- [Denoising] Noise2Void - Learning Denoising From Single Noisy Images, CVPR 2019.
- [Theory] Neural blind deconvolution using deep priors, CVPR 2020.
- [Restoration] CLEARER: Multi-Scale Neural Architecture Search for Image Restoration, 2020.
- [Theory] Neural architecture search with reinforcement learning, arXiv 2016.
- [Restoration] ISNAS-DIP: Image-Specific Neural Architecture Search for Deep Image Prior, arXiv 2021.
- [Restoration] Neural architecture search for deep image prior, Computers & Graphics 2021.
- [Restoration] "double-dip": Unsupervised image decomposition via coupled deep-image-priors, CVPR 2019.
- [Dehazing] Zero-shot image dehazing, IEEE TIP 2020.
- [Denoising] Self2Self With Dropout: Learning Self-Supervised Denoising From Single Image, CVPR 2020.
- [Denoising] Rethinking Deep Image Prior for Denoising, ICCV 2021.
- [Restoration] A bayesian perspective on the deep image prior, CVPR 2019.
- [Denoising] Self-Supervised Image Prior Learning With GMM From a Single Noisy Image, ICCV 2021.
- [Restoration] DeepRED: Deep image prior powered by RED, ICCVW 2019.
- [Restoration] Rare: Image reconstruction using deep priors learned without groundtruth, IEEE JSTSP 2020.
- [Denoising] Dynamic PET image denoising using deep image prior combined with regularization by denoising, IEEE Access 2021.
- [Video-Restoration] Blind video temporal consistency via deep video prior, NIPS 2020.
- [Video-Restoration] Deep Video Prior for Video Consistency and Propagation, IEEE TPAMI 2022.

## 2.4 Pre-trained Model as Prior

### 2.4.1 GAN Inversion as Prior
- [Theory] A style-based generator architecture for generative adversarial networks, CVPR 2019.
- [Super-Resolution] PULSE: Self-Supervised Photo Upsampling via Latent Space Exploration of Generative Models, CVPR 2020.
- [Super-Resolution] GLEAN: Generative Latent Bank for Large-Factor Image Super-Resolution, CVPR 2021.
- [Face-restoration] Towards real-world blind face restoration with generative facial prior, CVPR 2021.
- [Restoration] Exploiting Deep Generative Prior for Versatile Image Restoration and Manipulation, TPAMI 2021.

### 2.4.2 Generative Priors for Training Set Synthetic
- [Super-Resolution] To learn image super-resolution, use a gan to learn how to do image degradation first, ECCV 2018.
- [Super-Resolution] Unsupervised real-world image super resolution via domain-distance aware training, CVPR 2021.
- [Deblurring] Deblurring by realistic blurring, CVPR 2020.

### 2.4.3 Deep Denoiser Prior for Model-based Methods
- [Restoration] Learning deep CNN denoiser prior for image restoration, CVPR 2017.
- [Restoration] Plug-and-play image restoration with deep denoiser prior, TPAMI 2021.
- [Restoration] Denoising prior driven deep neural network for image restoration, TPAMI 2018.
- [Super-Resolution] Deep unfolding network for image super-resolution, CVPR 2020.

