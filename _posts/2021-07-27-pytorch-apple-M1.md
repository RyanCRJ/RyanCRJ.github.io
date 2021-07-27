---
layout: post
title: PyTorch Installation on Apple M1 Macs
subtitle: another flavor of deep learning using PyTorch
excerpt:
  PyTorch can be installed and run on Mac OS, including the M1 Mac. However, CUDA (GPU acceleration) is not currently supported on Apple M1 Mac.
cover-img:
thumbnail-img: /assets/img/pytorch.png
share-img: /assets/img/pytorch.png
tags: [platform, Apple M1]
comments: true
---
![TensorFlow](/assets/img/appleM1chip.png){: .mx-auto.d-block :}


## Install Miniforge

Assume that you have followed the previous post of _"TensorFlow Installation on Apple M1 Macs"_, installed Miniforge, and understood how to create a new Python environment through miniforge.

## Create a Python Environment for PyTorch

When creating a new Python environment by conda, you can use the [pytorch-apple-mac.yml](https://github.com/RyanCRJ/Machine_Learning/tree/main/Downloads) file I provided that specifies the dependencies. For PyTorch installation, we will need to use pip install of the local file [torch-1.8.0a0-cp39-cp39-macosx_11_0_arm64.whl](https://github.com/RyanCRJ/Machine_Learning/tree/main/Downloads). You should put both of these two files in the same folder and change the terminal diretory to the corresponding folder before executing the following steps.

create a python environment:
```zsh
conda env create -f pytorch-apple-mac.yml -n pytorch
```
enter this environment:
```zsh
conda activate pytorch
```
Install the PyTorch by the local
```zsh
pip install torch-1.8.0a0-cp39-cp39-macosx_11_0_arm64.whl
```
let's add Jupyter support to your new environment:
```zsh
conda install nb_conda
```

## Register your Environment
The following command registers your **pytorch** environment. Again, make sure you _"conda activate"_ your new **pytorch** environment.

```zsh
python -m ipykernel install --user --name pytorch --display-name "Python 3.9 (pytorch)"
```
<br/><br/>

### Notification

{: .box-note}
**Note:** CUDA (GPU acceleration) is not currently supported on Apple M1 Mac.
