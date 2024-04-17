# Ti-Patch
This repository implements the paper "Ti-Patch: Tiled Physical Adversarial Patch for no-reference video quality metrics" [[arxiv](https://arxiv.org/abs/2404.09961)]
![](https://github.com/leonenkova/Ti-Patch/raw/main/ims/DigitalAttachScheme.png)

## Datasets
For training, we selected 1000 256x256 images from the [COCO](https://www.kaggle.com/datasets/awsaf49/coco-2017-dataset) dataset. 
Validation was performed using 250 256x256 images from the COCO.

## Model
We attacked [PaQ-2-PiQ](https://github.com/baidut/paq2piq) NR image quality metric. 

## Code
To generate the Ti-Patch use the following [code](https://github.com/leonenkova/Ti-Patch/blob/main/Ti_Patch_Attack_Training.ipynb).

## Visualization
The examples of proposed patches:
![](https://github.com/leonenkova/Ti-Patch/blob/main/ims/Exmpls.png)
From left to right: Baseline, Baseline+TV+NPS, BaselineL, BaselineL+, B-WBaselineL+, B-WBaselineWRL+, BaselineWRL+(ours), BaselineWR(ours).

1) Baseline.
2) Baseline+TV+NPS: baseline with adding to the optimization TV loss and NPS loss.
3) BaselineL: baseline with additional adjustments to patch in the form of random changing brightness.
4) BaselineL+: baseline with TV loss and NPS loss and additional changing brightness.
5) B-WBaselineL+: BaselineL+ in black-white variant.
6) B-WBaselineWRL+: BaselineWRL+ in black-white variant.
7) BaselineWRL+(ours): baseline without rotation with TV loss and NPS loss and additional changing brightness.
8) BaselineWR(ours): baseline without random rotation patch while applying it on the image.


The example of wallpaper physical attack:
![](https://github.com/leonenkova/Ti-Patch/blob/main/ims/AdvWallpaperExp.gif)
