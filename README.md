# Diff-HMR: Diffusion-based Human Mesh Recovery

**This is the official PyTorch implementation of the approach described in the following paper:**
> [Generative Approach for Probabilistic Human Mesh Recovery using Diffusion Models](https://arxiv.org/abs/2111.15056?context=cs)\
> [Hanbyel Cho](https://scholar.google.com/citations?user=VvNXbu8AAAAJ&hl=ko) and [Junmo Kim](https://scholar.google.com/citations?hl=ko&user=GdQtWNQAAAAJ)\
> IEEE International Conference on Computer Vision (ICCV), 2023, [CV4Metaverse](https://sites.google.com/view/cv4metaverse/home?authuser=0) Workshop (submitted)

## Abstract
This work focuses on the problem of reconstructing a 3D human body mesh from a given 2D image. Despite the inherent ambiguity of the task of human mesh recovery, most existing works have adopted a method of regressing a single output. In contrast, we propose a generative approach framework, called "Diffusion-based Human Mesh Recovery (Diff-HMR)" that takes advantage of the denoising diffusion process to account for multiple plausible outcomes. During the training phase, the SMPL parameters are diffused from ground-truth parameters to random distribution, and Diff-HMR learns the reverse process of this diffusion. In the inference phase, the model progressively refines the given random SMPL parameters into the corresponding parameters that align with the input image. Diff-HMR, being a generative approach, is capable of generating diverse results for the same input image as the input noise varies. We conduct validation experiments, and the results demonstrate that the proposed framework effectively models the inherent ambiguity of the task of human mesh recovery in a probabilistic manner.

![qualitative_results](figs/qualitative_results.PNG)

## Dependencies
Make sure you have the following dependencies installed before proceeding:
- Python 3+ distribution
- PyTorch >= 0.4.0

## License
This work is licensed under CC BY-NC. See LICENSE for details. Third-party datasets are subject to their respective licenses.
If you use our code/models in your research, please cite our paper:
```
@InProceedings{Cho_2021_ICCV,
    author    = {Cho, Hanbyel and Cho, Yooshin and Yu, Jaemyung and Kim, Junmo},
    title     = {Camera Distortion-Aware 3D Human Pose Estimation in Video With Optimization-Based Meta-Learning},
    booktitle = {Proceedings of the IEEE/CVF International Conference on Computer Vision (ICCV)},
    month     = {October},
    year      = {2021},
    pages     = {11169-11178}
}
```

## Acknowledgement
Part of our code is borrowed from [SPIN](https://github.com/nkolot/SPIN) and [denoising-diffusion-pytorch](https://github.com/lucidrains/denoising-diffusion-pytorch).\
Please refer to their project pages for further information.
