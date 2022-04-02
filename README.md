<!--A curated list of resources for Image and Video Deblurring-->
<!-- PROJECT LOGO -->

<p align="center">
  <h3 align="center">Awesome-Image-Prior</h3>
  <p align="center">A curated list of resources for Prior in Image or Video 
    <br />
    <br />
    <br />
    <a href="https://github.com/yunfanLu/Awesome-Image-Prior/pulls/new">Suggest new item</a>
    <br />
    <a href="https://github.com/yunfanLu/Awesome-Image-Prior/issues/new">Report Bug</a>
  </p>
</p>

# Image Enhancement Classification

![](ImageEnhancement.png)

# Prior Classification

![](./ImagePrior.png)



# 1.Handcrafted Prior

## 1.1 Regularization

### 1.1.1 Total Variation Regularization

**Definition:** Total variation regularization or total variation filtering, is a noise removal process (filter). It is based on the principle that signals with excessive and possibly spurious detail have high total variation, that is, the integral of the absolute image gradient is high. 

**Tasks:** Deblur; 

| Deblur | Total variation blind deconvolution | TIP  |
| :----- | ----------------------------------- | ---- |
|        |                                     |      |



### 1.1.2 L 0-regularized prior

**Definintion:** L 0-regularized describes the sparsity of image pixels.

**Task:** Deblur; Dehazing;

| Deblur | Unnatural L 0sparse representation for natural image deblurring | CVPR 2013 |
| ------ | ------------------------------------------------------------ | --------- |
| Deblur | L 0-regularized intensity and gradient prior for deblurring text images and beyond | PAMI 2016 |



## 1.2 Gradient

### 1.2.1 Heavy-tailed gradient distributions

**Definition:**

**Task: ** Deblur;

| Deblur | Removing camera shake from a single photograph              | SIGGRAPH 2006 |
| ------ | ----------------------------------------------------------- | ------------- |
| Deblur | Understanding and evaluating blind deconvolution algorithms | CVPR 2009     |



### 1.2.2 Local Maximum Gradient (LMG) prior

## 1.3  Optical flow

**Definition:** Optical flow or optic flow is the pattern of apparent motion of objects, surfaces, and edges in a visual scene caused by the relative motion between an observer and a scene. 

**Tasks:** Deblur; Image/Video SR;

| SR   | Video Enhancement with Task-Oriented Flow                    | IJCV 2019  |
| ---- | ------------------------------------------------------------ | ---------- |
| SR   | Frame-Recurrent Video Super-Resolution                       | CVPR 2018  |
| SR   | BasicVSR++: Improving Video Super-Resolution with Enhanced Propagation and Alignment | NTIRE 2021 |
| SR   | BasicVSR: The Search for Essential Components in Video Super-Resolution and Beyond | CVPR 2021  |



### 1.3.1 Temporal sharpness prior

## 1.4 Data Description

### 1.4.1 RGB to Wavelet

### 1.4.2 RGB to frequency

### 1.4.3 Facial prior

## 1.5 Color Description

### 1.5.1Gamma Correction

### 1.5.2 Color Ellipsold 

### 1.5.3 Average Saturation

### 1.5.4 Histogram Destribution 

### 1.5.5 Color Attenuation Priro

# 2. Latent Prior

## 2.1 Patten

### 2.1.1 Light Streaks

### 2.1.2 Global Similarity Prior

### 2.1.3 Strong Edges

### 2.1.4 Blurry Image Outlies

## 2.2 Recurrences

### 2.2.1 Patch Recurrences

**Definition:**

**Tasks:** Image/Video SR;

| SR   | Super-resolution from a single image | CVPR 2009 |
| ---- | ------------------------------------ | --------- |
|      |                                      |           |



## 2.3 Scienes

### 2.3.1 3D facial Prior

**Definition:** Utilize the 3D information of the face for human

**Tasks:** Deblur;

| Deblur | Face video deblurring using 3D facial priors | ICCV 2019 |
| ------ | -------------------------------------------- | --------- |
|        |                                              |           |

### 2.3.2 Nature Environment

#### 2.3.2.1 Illumination Prior

#### 2.3.2.2 Non-Uniform

#### 2.3.2.3 Atmospheric illumination

### 2.3.3 Noise Pattern

## 2.4 Statistics

### 2.4.1 Gradient Channels

### 2.4.2 Extreme Channels

#### 2.4.2.1 Dark Channels

**Defination:** The dark channel prior is a kind of statistics of outdoor haze-free images. It is based on a key observation—most local patches in outdoor haze-free images contain some pixels whose intensity is very low in at least one color channel.

**Tasks:** Deblur; Dehazing;

| Low Light Enhancement | Night video enhancement using improved dark channel prior    | 2013                             |
| --------------------- | ------------------------------------------------------------ | -------------------------------- |
| Dehazing              | Unsupervised Single Image Dehazing Using Dark Channel Prior Loss | TIP2018                          |
| Dehazing              | Dehazing of remote sensing images using improved restoration model based dark channel prior | The Imaging Science Journal 2017 |



#### 2.4.2.2 Light Channels

### 2.4.3 Bounded Channel Difference

### 2.4.4 Blur Channel Prior

## 2.5 Deep Prior

### 2.5.1 Deep Image Prior

**Defination:** Deep Image Prior is a type of convolutional neural network used to enhance a given image with no prior training data other than the image itself. 

**Tasks:** Denoising; Image Restoration; HDR; 

| Denoise           | Patchdip exploiting patch redundancy in deep image prior for denoising | NIPS 2019    |
| ----------------- | ------------------------------------------------------------ | ------------ |
| Image Restoration | BP-DIP: A Backprojection based Deep Image Prior              | EUSIPCO 2020 |
| Image Restoration | Image restoration using total variation regularized deep image prior | ICASSP  2019 |
| Defense           | Exploring Properties of the Deep Image Prior                 | NIPS 2019    |
| HDR               | High dynamic range imaging using deep image priors           | 2020         |
| Denoise           | Deep Image Prior                                             | CVPR         |



### 2.5.2 Deep Video Prior

Definition: 

Tasks:

| Flickering Artifact | Blind video temporal consistency via deep video prior | NIPS 2020 |
| ------------------- | ----------------------------------------------------- | --------- |
|                     | Deep Video Prior                                      | NIPS 2020 |



## 2.6 Semantic