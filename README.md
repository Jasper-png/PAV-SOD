# Panoramic Audiovisual Salient Object Detection



# Introduction

<p align="center">
    <img src="./figures/fig_teaser_v2.jpg"/> <br />
    <em> 
    Figure 1: An example of our PAVS10K where coarse-to-fine annotations are provided, based on a guidance of fixations acquired from subjective experiments conducted by multiple (N) subjects wearing Head-Mounted Displays (HMDs) and headphones. Each (e.g., fk, fl and fn, where random integral values {k, l, n} ∈ [1, T ]) of the total equirectangular (ER) video frames T of the sequence “Speaking”(Super-class)-“Brothers”(sub-class) are manually labeled with both object-level and instance-level pixel-wise masks. According to the features of defined salient objects within each of the sequences, multiple attributes, e.g., “multiple objects” (MO), “competing sounds” (CS), “geometrical distortion” (GD), “motion blur” (MB), “occlusions” (OC) and “low resolution” (LR) are further annotated to enable detailed analysis for PAV-SOD modeling.
    </em>
</p>

Object-level audiovisual saliency detection in 360° panoramic real-life dynamic scenes is important for exploring and modeling human perception in immersive environments, also for aiding the development of virtual, augmented and mixed reality applications in the fields of such as education, social network, entertainment and training. To this end, we propose a new task, panoramic audiovisual salient object detection (PAV-SOD), which aims to segment the objects grasping most of the human attention in 360° panoramic videos reflecting real-life daily scenes. To support the task, we collect PAVS10K, the first panoramic video dataset for audiovisual salient object detection, which consists of 67 4K-resolution equirectangular videos with per-video labels including hierarchical scene categories and associated attributes depicting specific challenges for conducting PAV-SOD, and 10,465 uniformly sampled video frames with manually annotated object-level and instance-level pixel-wise masks. The coarse-to-fine annotations enable multi-perspective analysis regarding PAV-SOD modeling. We further systematically benchmark 13 state-of-the-art salient object detection (SOD)/video object segmentation (VOS) methods based on our PAVS10K. Besides, we propose a new baseline model, i.e., CAV-Net, which takes advantage of both visual and audio cues of 360 video frames by using a new conditional variational auto-encoder. As a result, our CAV-Net outperforms all competing models and is able to represent the data bias within PAVS10K via uncertainty estimation. With extensive experimental results, we gain several findings about PAV-SOD challenges and insights towards PAV-SOD model interpretability. We hope that our work could serve as a starting point for advancing SOD towards immersive media.


:running: :running: :running: ***KEEP UPDATING***.

------

# Related Dataset Works

<p align="center">
    <img src="./figures/fig_related_works.jpg"/> <br />
    <em> 
    Figure 2: Summary of widely used salient object detection (SOD) datasets and the proposed panoramic video SOD (PV-SOD) dataset. #Img: The number of images/frames. #GT: The number of ground-truth masks. Pub. = Publication. Obj.-Level = Object-Level. Ins.-Level = Instance-Level. Fix.GT = Fixation-guided ground truths. † denotes equirectangular (ER) images.
    </em>
</p>

------

# Dataset Annotations and Attributes

<p align="center">
    <img src="./figures/fig_attributes.jpg"/> <br />
    <em> 
    Figure 3: Examples of challenging attributes on equirectangular (ER) images from our ASOD60K, with instance-level GT and fixations as annotation guidance. f(k,l,m) denote random frames of a given video.
    </em>
</p>


<p align="center">
    <img src="./figures/fig_pass_reject.jpg"/> <br />
    <em> 
    Figure 4: More annotations. Passed and rejected examples of annotation quality control.
    </em>
</p>


<p align="left">
    <img src="./figures/fig_attr_statistics.jpg"/> <br />
    <em> 
    Figure 5: Attributes description and stastistics. (a)/(b) represent the correlation and frequency of ASOD60K’s attributes, respectively.
    </em>
</p>



# Dataset Statistics 

<p align="center">
    <img src="./figures/fig_categories.jpg"/> <br />
    <em> 
    Figure 6: Statistics of the proposed ASOD60K. (a) Super-/sub-category information. (b) Instance density of each sub-class. (c) Main components of ASOD60K scenes.
    </em>
</p>


------

# Benchmark

## Overall Quantitative Results

<p align="center">
    <img src="./figures/fig_quantitative_results.jpg"/> <br />
    <em> 
    Figure 7: Performance comparison of 7/3 state-of-the-art conventional I-SOD/V-SOD methods and one PI-SOD method over ASOD60K. ↑/↓ denotes a larger/smaller value is better. Best result of each column is bolded.
    </em>
</p>

## Attributes-Specific Quantitative Results

<p align="center">
    <img src="./figures/fig_attr_quantitative_results.jpg"/> <br />
    <em> 
    Figure 8: Performance comparison of 7/3/1 state-of-the-art I-SOD/V-SOD/PI-SOD methods based on each of the attributes.
    </em>
</p>

## Reference

**No.** | **Year** | **Pub.** | **Title** | **Links** 
:-: | :-: | :-: | :-  | :-: 
01 | 2019 | IEEE CVPR   |  Cascaded Partial Decoder for Fast and Accurate Salient Object Detection | [Paper](https://openaccess.thecvf.com/content_CVPR_2019/papers/Wu_Cascaded_Partial_Decoder_for_Fast_and_Accurate_Salient_Object_Detection_CVPR_2019_paper.pdf)/[Project](https://github.com/wuzhe71/CPD)
02 | 2019 | IEEE ICCV |  Stacked Cross Refinement Network for Edge-Aware Salient Object Detection | [Paper](https://openaccess.thecvf.com/content_ICCV_2019/papers/Wu_Stacked_Cross_Refinement_Network_for_Edge-Aware_Salient_Object_Detection_ICCV_2019_paper.pdf)/[Project](https://github.com/wuzhe71/SCRN)
03 | 2020 | AAAI   |  F3Net: Fusion, Feedback and Focus for Salient Object Detection | [Paper](https://arxiv.org/pdf/1911.11445.pdf)/[Project](https://github.com/weijun88/F3Net)
04 | 2020 | IEEE CVPR  |  Multi-scale Interactive Network for Salient Object Detection | [Paper](https://openaccess.thecvf.com/content_CVPR_2020/papers/Pang_Multi-Scale_Interactive_Network_for_Salient_Object_Detection_CVPR_2020_paper.pdf)/[Project](https://github.com/lartpang/MINet)
05 | 2020 | IEEE CVPR |  Label Decoupling Framework for Salient Object Detection | [Paper](https://openaccess.thecvf.com/content_CVPR_2020/papers/Wei_Label_Decoupling_Framework_for_Salient_Object_Detection_CVPR_2020_paper.pdf)/[Project](https://github.com/weijun88/LDF)
06 | 2020 | ECCV       |  Highly Efficient Salient Object Detection with 100K Parameters | [Paper](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123510698.pdf)/[Project](https://github.com/ShangHua-Gao/SOD100K)
07 | 2020 | ECCV       |  Suppress and Balance: A Simple Gated Network for Salient Object Detection | [Paper](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123470035.pdf)/[Project](https://github.com/Xiaoqi-Zhao-DLUT/GateNet-RGB-Saliency)
08 | 2019 | IEEE CVPR |  See More, Know More: Unsupervised Video Object Segmentation with Co-Attention Siamese Networks | [Paper](https://openaccess.thecvf.com/content_CVPR_2019/papers/Lu_See_More_Know_More_Unsupervised_Video_Object_Segmentation_With_Co-Attention_CVPR_2019_paper.pdf)/[Project](https://github.com/carrierlxk/COSNet)
09 | 2019 | IEEE ICCV |  Semi-Supervised Video Salient Object Detection Using Pseudo-Labels | [Paper](https://openaccess.thecvf.com/content_ICCV_2019/papers/Yan_Semi-Supervised_Video_Salient_Object_Detection_Using_Pseudo-Labels_ICCV_2019_paper.pdf)/[Project](https://github.com/Kinpzz/RCRNet-Pytorch) 
10 | 2020 | AAAI     |  Pyramid Constrained Self-Attention Network for Fast Video Salient Object Detection | [Paper](http://mftp.mmcheng.net/Papers/20AAAI-PCSA.pdf)/[Project](https://github.com/guyuchao/PyramidCSA) 
11 | 2020 | IEEE SPL     |  FANet: Features Adaptation Network for 360° Omnidirectional Salient Object Detection | [Paper](https://ieeexplore.ieee.org/abstract/document/9211754)/[Project](https://github.com/DreaMKHuang/FANet) 

------

# CAV-Net (Baseline Model)

(release soon)

------

# Evaluation Toolbox

All the quantitative results were computed based on one-key Python toolbox: https://github.com/zzhanghub/eval-co-sod .

------

# Downloads

The whole object-/instance-level ground truth with default split can be downloaded from [Baidu Dirve](https://pan.baidu.com/s/1zDXE9iHGyWZFFUDIeaKIdQ)(k3h8) or [Google Drive](https://drive.google.com/file/d/1SjsYz57gArBVr_yzgcRnqYI4MpDiZ_Fh/view?usp=sharing).

The videos with default split can be downloaded from [Google Drive](https://drive.google.com/file/d/1qYnXwKLZUtn4Gb8R9U5P4qsibUCNGoUN/view?usp=sharing) or [OneDrive](https://1drv.ms/u/s!Ais1kZo7RR7Lg1Vt1cA_M05apzL7?e=PzZ4Va). 

The head movement and eye fixation data can be downloaded from [Google Drive](https://drive.google.com/drive/folders/1tZDIESRiy3W2g--8lnNWag3KhpEGqTHc?usp=sharing)

To generate video frames, please refer to [video_to_frames.py](https://github.com/PanoAsh/ASOD60K/blob/main/video_to_frames.py).

To get access to raw videos on YouTube, please refer to [video_seq_link](https://github.com/PanoAsh/ASOD60K/blob/main/video_seq_link). 

To check basic information regarding the raw videos, please refer to [video_information.txt](https://github.com/PanoAsh/ASOD60K/blob/main/video_information.txt) (keep updating).

------

# Contact

For any problems, please open an [issue](https://github.com/PanoAsh/ASOD60K/issues/new).

Specifically,

If you have any question on head movement and eye fixation data, please contact fang-yi.chao@tcd.ie

