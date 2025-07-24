# Towards Arbitrary-Scale Image Super-Resolution with Prompting and Diffusion Prior (ProDiff)
**The official repository with Pytorch**

## Installation
**Clone this repo:**
```bash
git clone https://github.com/GuangYuanKK/ProDiff.git
cd ProDiff
```
**Dependencies:**
- python3.7+
- pytorch
- pyyaml, scipy, tqdm, imageio, einops, opencv-python
- cupy

You can run the following command
```
conda env create -f environment.yaml
```

## Training
We divide the training into two stages.
-  Phase 1
Modify the dataset path in options/train/train_ProDiff_S1.xml, and run the following command to train.
```
CUDA_VISIBLE_DEVICES=0 python train.py -opt options/train/train_ProDiff_S1.yml
```
-  Phase 2
Modify the paths of the datasets and the location of the pretrained model in the configuration file.
```
CUDA_VISIBLE_DEVICES=0 python train.py -opt options/train/train_ProDiff_S2.yml
```

## Test
Modify the dataset path and pre-trained model path in options/test/test*.xml, and run the following command to test.
```
CUDA_VISIBLE_DEVICES=0 python test.py -opt options/test_ours/test*.yml
```

### Pretrained Models
Coming Soon
