# NTIRE 2023: Light Field Image Super-Resolution Challenge <br> 
<p align="center">  <img src="https://raw.github.com/YingqianWang/Awesome-LF-Image-SR/master/Fig/Thumbnail.jpg" width="1000"> </p>

**Light field (LF) image super-resolution (SR) challenge is held as a part of the [NTIRE workshop](https://data.vision.ee.ethz.ch/cvl/ntire23/) in conjunction with CVPR 2023. The goal of this challenge is to develop methods to enhance the spatial resolution of LF images.**


## News and Updates:
* **2022-12-16**: The proposal for LF image SR challenge is approved.

## Introduction
With recent advances in camera manufacturing, light field (LF) imaging technology becomes increasingly popular and is commonly used in various applications such as mobile phones, biological microscope, VR/AR etc. Since both intensity and directions of light rays are recorded by LF cameras, the resolution of LF images can be enhanced by using these additional angular information. LF image super-resolution (SR), also known as LF spatial SR, aims at reconstructing high-resolution (HR) LF images from their low-resolution (LR) counterparts. 

Jointly with the NTIRE workshop, we have a challenge for LF community to focus on enhancing the spatial resolution of LF images, and aspire to highlight the specific challenges and research problems faced by LF image SR. This challenge provides an opportunity for researchers to work together to share their knowledge and insights, advance the algorithm performance, and promote the development of LF image SR.


## Challenge Overview
The objective of this challenge is to reconstruct high-resolution (HR) LF images from their low-resolution (LR) counterparts.

During the model development phase, the training set and the validation set will be released. Both HR LF images and their LR counterparts in the training and validation sets are available. The participants can train their models on the training set and can evaluate their models with the validation set.

During the test phase, the test set will be released, which includes LR LF images only. Challenge participants should apply their trained models to the LR test images to generate super-resolved test images. These super-resolved images will then be submitted by the participants and evaluated by the organizers with a set of objective quantitative metrics.


## Datasets
### Training Set: *[[Baidu Drive](https://pan.baidu.com/s/1mYQR6OBXoEKrOk0TjV85Yw) (key:7nzy) or [OneDrive](https://stuxidianeducn-my.sharepoint.com/:f:/g/personal/zyliang_stu_xidian_edu_cn/EpkUehGwOlFIuSSdadq9S4MBEeFkNGPD_DlzkBBmZaV_mA?e=FiUeiv)]*

This challenge follows the training set in the paper [LF-InterNet](https://arxiv.org/pdf/1912.07849), and uses the EPFL, HCInew, HCIold, INRIA and STFgantry datasets consisting of 144 scenes for training. All the LF images in the training set have an angular resolution of 9x9. Both HR LF images and their LR versions (produced by bicubic downsampling) are released. The participants can use these HR LF images as groundtruths to train their models. More details of the training set can be refered to [BasicLFSR](https://github.com/ZhengyuLiang24/BasicLFSR). 


### Validation Set: *[[Baidu Drive]() (key:) or [OneDrive]()]*

We collect a new validation set consisting of 10 synthetic scenes blended by the 3Ds MAX software and 10 real-world images captured by a Lytro ILLUM camera. Both HR and LR images with an angular resolution of 5x5 in the validation set are provided. The participants can download the validation set to evaluate the performance of their developed models by comparing their super-resolved images with the HR groundtruth images. **Note that, the validation set should be used for validation purpose only but cannot be used as additional training data.** The participants are encouraged to write papers to describe their methods and use the released validation set for performance evaluation.


### Test Set: *[[download LR test data](https://www.jianguoyun.com/p/DWQY4hYQwOebChjh37QE)]*

We collect a new test set consisting of 10 synthetic scenes blended by the 3Ds MAX software and 10 real-world images captured by a Lytro ILLUM camera. Different from the training and validation sets, only LR LF images with an angular resolution of 5x5 will be released. The participants are required to apply their models to the released LR LF images and submit their super-resolved images to the CodaLab platform for metrics scoring. **It should be noted that the images in the test set (even the LR versions) cannot be used for training.**


## Evaluation Metrics
We evaluate the submitted results by comparing them with the ground truth LF image pairs. To measure the fidelity, we use the standard Peak Signal to Noise Ratio (PSNR) and, complementarily, the Structural Similarity (SSIM) index as they are often employed in the literature. PSNR and SSIM implementations can be found in most of the image processing toolboxes. **We report the submissions over the synthetic and real-world images in the test sets, and rank the submissions according to the average PSNR values.**
The SSIM metrics will not affect submission rankings but will be used to review the strengths and weaknesses of suggested methods in the final challenge report. 


## Baseline Model
Over the last few years, several milestone methods have been developed for LF image SR, including [LF-InterNet](https://github.com/YingqianWang/LF-InterNet), [LF-DFnet](https://github.com/YingqianWang/LF-DFnet),  [MEG-Net](https://github.com/shuozh/MEG-Net), [LFT](https://github.com/ZhengyuLiang24/LFT) and [DistgSSR](https://github.com/YingqianWang/DistgSSR). In this challenge, **LF-InterNet** is used as a baseline model and the submitted results should be at least on par with LF-InterNet. The solutions with PSNR values lower than LF-InterNet will not be ranked in the leaderboard.


### PSNR and SSIM values achieved by baseline methods on the validation set for 4xSR:
| Method | PSNR (avg)  |  PSNR (syn)  | PSNR (real)  || SSIM (avg)  |  SSIM (syn)  | SSIM (real)  |
|:------:|  :--------: | :--------: | :---------: | :-------: | :-------: | :-------: | :-------: |
| Bicubic       | 
| LF-InterNet   | 

## Submission
We use [CodaLab](https://codalab.lisn.upsaclay.fr/competitions/1598) for online submission in the development phase. **Here, we provide an example ([Jianguoyun Drive](https://www.jianguoyun.com/p/DXWimH4QwOebChipxasE) or [Google Drive](https://drive.google.com/file/d/1gyaan54AwbAYLIIA1rly_wrLzdyQ7VAh/view?usp=sharing)) to help participants to format their submissions.** In the test phase, the final results and the source codes (both training and test) need to be submitted via emails (ntire.stereosr@outlook.com). Please refer to our [online website](https://codalab.lisn.upsaclay.fr/competitions/1598) for details of the submission rules.

## Important Dates
* 2022-12-16: The proposal for LF image SR challenge is approved;


## Group number policy
Each group cannot have more than six group members (i.e., 1 to 6 group members is OK), and each paricipant can only join one group. Each group can only submit one algorithm for final ranking.


## Issues and Questions:
For any question regarding this challenge, raise an issue under this repository. <br>
You can also join our WeChat group by scanning the code below:

<p align="center"> <img src="https://raw.github.com/The-Learning-And-Vision-Atelier-LAVA/Stereo-Image-SR/NTIRE2022/Fig/WeChat.jpg" width="30%"> </p>

## Organizers:
* [**Yulan Guo**](http://yulanguo.me/) ([yulan.guo@nudt.edu.cn](yulan.guo@nudt.edu.cn))
* [**Longguang Wang**](https://longguangwang.github.io/) ([wanglongguang15@nudt.edu.cn](wanglongguang15@nudt.edu.cn))
* [**Yingqian Wang**](https://yingqianwang.github.io/) ([wangyingqian16@nudt.edu.cn](wangyingqian16@nudt.edu.cn))
* [**Juncheng Li**](https://junchenglee.com/) ([junchengli@math.cuhk.edu.hk](junchengli@math.cuhk.edu.hk))
* [**Shuhang Gu**](https://shuhanggu.github.io/) ([shuhanggu@gmail.com](shuhanggu@gmail.com))
* [**Radu Timofte**](https://people.ee.ethz.ch/~timofter/) ([Radu.Timofte@vision.ee.ethz.ch](Radu.Timofte@vision.ee.ethz.ch))

## Acknowledgement:
We would like to thank **<a href="https://www.flickr.com/photos/stereotron/" target="_blank">Sascha Becher</a>**
 and **<a href="https://www.flickr.com/photos/tombentz" target="_blank">Tom Bentz</a>** for the approval of using their cross-eye stereo photographs. <br>

## NTIRE 2022 Terms and Conditions:
The terms and conditions of this challenge can be viewed [here](https://codalab.lisn.upsaclay.fr/competitions/1598#learn_the_details-terms_and_conditions).


