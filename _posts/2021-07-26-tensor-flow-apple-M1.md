---
layout: post
title: TensorFlow Installation on Apple M1 Macs
subtitle: power your M1 chip for deep learning
excerpt:
  The M1 chip in Apple's latest Mac contains a powerful new 8-Core CPU and up to 8-core GPU that are optimized for ML training tasks right on the Mac.
thumbnail-img: /assets/img/apple_m1.jpg
share-img: /assets/img/apple_m1.jpg
tags: [platform, Apple M1]
comments: true
---
![TensorFlow](/assets/img/tensorflow.png){: .mx-auto.d-block :}

The M1 chip in Apple's latest Mac contains a powerful new 8-Core CPU and up to 8-core GPU that are optimized for ML training tasks right on the Mac. You can check out this blog for the [comparison of ML training performance between M1 Mac and prior models](https://blog.tensorflow.org/2020/11/accelerating-tensorflow-performance-on-mac.html).

## Install TensorFlow through Miniforge

The [installation steps](https://github.com/jeffheaton/t81_558_deep_learning/blob/master/install/tensorflow-install-mac-metal-jul-2021.ipynb) of TensorFlow2.5 on M1 Mac is fairly simple. You can check out this [YouTube video](https://www.youtube.com/watch?v=_CO-ND1FTOU) for step-by-step guidance created by Prof. Jeff Heaton from Washington University in St. Louis.

## Activate the Python Environment for TensorFlow

Once you successfully installed the tensorflow, you can activate/deactivate the conda env of python where the tensorflow is installed, inside the terminal window.

activate/deactivate conda environment:
```zsh
conda activate tensorflow
conda deactivate
```
check python environment:
```zsh
which python
```

## Configure the Python Environment in Atom Editor

If we want to run a python script from text editor, such as [Atom](https://atom.io), we can specify the python version or environment to use.  

Firstly, we need to install a Atom package, [script](https://atom.io/packages/script), that allows running code in Atom.

The next step is to set the _**command**_ in configuration to a specific python path and then _**save as profile**_.

![Atom](/assets/img/atom_scripts.png)

Next time, you can run with the same profile by <kbd>Shift</kbd>+<kbd>Cmd</kbd>+<kbd>K</kbd>.

For more details, you can watch this YouTube video for [Setting up a Python Development Environment in Atom](https://www.youtube.com/watch?v=DjEuROpsvp4&t=8s).
