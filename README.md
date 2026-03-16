# Supplementary materials for: 
# Multi-Guide: Detecting Unreliable DNN Outputs with Local and Global Score Complementarity

## This zip contains:
- The supplementary material document.
- UNNGuide implementation.

## Instruction for executing UNNGuide:
### Prerequisite:

To execute UNNGuide, you must have the following software installed (the versions are the recommended ones):

- Python 3.11.4
- R 4.3.3
- Jupyter Notebook 6.5.4
- CUDA with cudnn (To support the corresponding pytorch platform), you should have an NVIDIA graphics card (e.g., CUDA 11.8 with NVIDIA GeForce RTX 4080 Laptop GPU).

The required libraries for Python are listed in the file requirements.txt in the folder "code."

### ID and OOD datasets
It is important to configure the following datasets before initiating the experiments:
- Please follow the guide in https://github.com/deeplearning-wisc/dice to download the OOD datasets for CIFAR10 and CIFAR100, you should put them in a folder named "datasets" in the folder "src".
- Please follow the guides in https://github.com/deeplearning-wisc/dice and https://github.com/roomo7time/nnguide?tab=readme-ov-file (for OpenImage-O) to download the OOD datasets for Imagenet, the OpenImage-O images should be placed in the following path "datasets\ood_datasets\OpenImage-O\images". The OOD datasets should be in a folder named "datasets" in the folder "src".
- Please download the Imagenet-1K (ILSVRC2012: https://www.kaggle.com/c/imagenet-object-localization-challenge/overview/description) and reform the validation set to the classification problem format that can be accepted by the pytorch class "ImageFolder".

### Pretrained models
It is also important to dowload the pretrained models to be able to launch the experiments:
- Download the "experim_models_UNNGuide.zip," which contains the pre-trained ResNet models from ..., and extract it in the folder "src." The sub-folders should be directly presented in the folder "src" (i.e., without a parent folder named "experim_models_UNNGuide").

### Launch UNNGuide

To launch the experiment, you should:

1. Go to the "src" folder and open a terminal.
2. Type the command "jupyter notebook."
3. Open the notebook you would like to run (e.g., UNNGuide_CIFAR10_DenseNet_101_OOD_Detection.ipynb).
4. Configure the parameters required in the notebook (Generally only for the data path of the Imagenet dataset).
5. Launch the notebook.
