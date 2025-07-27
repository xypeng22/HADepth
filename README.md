# HADepth

This is the official PyTorch implementation of the method  as described in

"HADepth: Highlight-aware monocular depth estimation for endoscopy" submitted to **Signal, Image and Video Processing**.

![Image](assets/network.png)

## ⚙️ Setup

Our experimental configuration and hyperparameters are as follows:

| Parameter             | Configuration           |
| --------------------- | ----------------------- |
| CPU                   | Intel Core i9-10980XE   |
| GPU                   | NVIDIA GeForce RTX 3090 |
| Operating system      | Ubuntu 20.04.5 LTS      |
| CUDA                  | 11.7                    |
| Python version        | 3.9.17                  |
| PyTorch version       | 1.13.0                  |
| Batch size            | 8                       |
| Epochs                | 20                      |
| Initial learning rate | 0.0001                  |
| Optimizer             | Adam                    |

## 💾 Datasets

The datasets are publicly available at the following URLs:  

**SCARED**: https://endovissub2019-scared.grand-challenge.org/

**ColonDepth**: http://cmic.cs.ucl.ac.uk/ColonoscopyDepth/

For more details on the dataset acquisition of SCARED, please refer to the instructions provided in  [AF-SfMLearner](https://github.com/ShuweiShao/AF-SfMLearner).

## 📊 Evaluation

We are currently organizing the code section, and the testing portion of the code will be made publicly available soon.

|        Method        | Abs Rel ↓ | Sq Rel ↓ | RMSE ↓ | RMSE log ↓ | &delta; ↑ |
|:--------------------:|:---------:|:--------:| ------ | ---------- |:---------:|
|      Monodepth2      | 0.071     | 0.590    | 5.606  | 0.094      |           |
| Endo-SfMLearner | 0.062     | 0.606    | 5.726  | 0.093      |           |
|  AF-SfMLearner | 0.059     | 0.435    | 4.925  | 0.113      |           |
| EndoDepth-Perf | 0.094     | 0.635    | 5.229  | 0.081      |           |
| IID-SfMLearner | 0.057     | 0.413    | 4.796  | 0.079      |           |
| Depth Anything | 0.058     | 0.451    | 5.058  | 0.081      |           |
|     EndoDAC    | 0.051     | 0.355    | 4.436  | 0.073      |           |
|     Ours       |           |          |        |            |           |

## 📦 Pretrained Models

We have released our pretrained models in this link: [google drive ](https://drive.google.com/drive/folders/1vCzhDq-d8ZvCebPcQR6I0IjMf10u6mxM?usp=sharing).

## Acknowledgement

We thank the authors of [AF-SfMLearner](https://github.com/ShuweiShao/AF-SfMLearner), [IID-SfMLearner](https://github.com/bobo909/IID-SfmLearner), [Depth Anything](https://github.com/LiheYoung/Depth-Anything) and [EndoDAC](https://github.com/BeileiCui/EndoDAC) for opening source their code.