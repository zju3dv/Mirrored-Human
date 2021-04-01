<div align="center">
    <img src="doc/assets/logo.jpg" width="250">
</div>

-----------------

# Reconstructing 3D Human Pose by Watching Humans in the Mirror

> [![](https://img.shields.io/badge/homepage-brightgreen)](https://zju3dv.github.io/Mirrored-Human/) [![report](https://img.shields.io/badge/arxiv-link-red)](https://arxiv.org/abs/0000.00000)  
> Qi Fang\*, Qing Shuai\*, Junting Dong, Hujun Bao, Xiaowei Zhou  
> CVPR 2021 Oral

<div align="center">
    <img src="doc/assets/smpl-avatar.gif" width="80%">
</div>
<div align="center">
    <img src="doc/assets/calorie.gif" width="40%">
    <img src="doc/assets/imitate.gif" width="40%">
    <br>
    <sup>The videos are from <a href="https://www.youtube.com/watch?v=KOCJJ27hhIE">Youtube<a/> and Douyin, please contact us for any problems of copyright.</sup>
</div>


## Features  
In this paper, we introduce the new task of reconstructing 3D human pose from a single image in which we can see the person  and the person’s image through a mirror.

This implementation:

- has the demo of our optimization-based approach implemented purely in PyTorch.
- provides a method to estimate the surface normal of the mirror from vanishing points.
- provides an annotator to label the mirror edges for the vanishing points.
- can estimate the focal length of the Internet mirror images.

## Installation  
This repo has a close relation with EasyMocap. Please refer to our [EasyMocap](https://github.com/zju3dv/EasyMocap) project for installation.

## Demo
Download our [data/sample-videos.zip](./data/sample-videos.zip)  and run the following code:
```bash
# set the data path
data=<path_to_sample>/sample-videos
out=<path_to_sample>/sample-videos-output
# extract the video frames
python3 scripts/preprocess/extract_video.py ${data}
# Run demo on videos
python3 easymocap/demo_1v1pmf_smpl_mirror.py ${data} --out ${out} --video --vis_smpl
```

## Mirrored-Human Dataset (Coming Soon)
Due to the license limitation, we cannot share the raw data directly. We are working hard to organize the Mirrored-Human dataset in terms of url links and timestamps.

<div align="center">
  <img src="doc/assets/dataset_show.jpg" width="70%" />
</div>


## Evaluation  
To evaluate the reconstruction part in our paper, see [doc/evaluation.md](doc/evaluation.md).

## Annotator (Coming Soon)

See [doc/annotator.md](doc/annotator.md) for more instructions.

## Build Custom Internet Dataset (Mirror)
See [doc/internet.md](doc/internet.md) for more instructions.

## Build Custom Evaluation Dataset (Multi-View)  
See [doc/custom.md](doc/custom.md) for more instructions.

<div align="center">
  <img src="doc/assets/000530_mesh.jpg" width="70%" />
</div>


## Contact  
Please open an issue if you have any questions. We appreciate all contributions to improve our project.

## Citation

```
@inproceedings{fang2021mirrored,
  title={Reconstructing 3D Human Pose by Watching Humans in the Mirror},
  author={Fang, Qi and Shuai, Qing and Dong, Junting and Bao, Hujun and Zhou, Xiaowei},
  booktitle={CVPR},
  year={2021}
}
```

## Acknowledgement  
This project is build on our [EasyMocap](https://github.com/zju3dv/EasyMocap). We also would like to thank Jianan Zhen and Yuhao Chen for their advice for the paper. Sincere thanks to the performers (Yuji Chen and Hao Xu) in the evaluation dataset and people who uploaded the mirror-human videos to the Internet.

## Recommendations to other works from our group  
Welcome to checkout our work on learning-based feature matching ([LoFTR](https://zju3dv.github.io/loftr/index.html)) and reconstruction ([NeuralBody](https://zju3dv.github.io/neuralbody/) and [NeuralRecon](https://zju3dv.github.io/neuralrecon/)) in CVPR 2021.
