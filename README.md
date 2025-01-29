# GLSD
This is the Pytorch implementation of GLSD for remote sensing scene image classification.

# Requirements
Python 3.8, Pytorch 2.4, CUDA 12.4

# Usage
## Data preparation

## Training model

# Experimental results
all the experiments are implemented by Pytorch 2.4.1 Version in the computing environment of 1 × 24-GB NVIDIA GeForce RTX 4090 GPU. In order to obtain reliable experimental results, we randomly divided the dataset using the same training ratio on each dataset, repeated the experiment five times, and reported the mean and standard deviation of these results. The `train.log` and `model.pth` of each result are provided.
## AID
| model | AID_20%_1 | AID_20%_2 | AID_20%_3 | AID_20%_4 | AID_20%_5 | mean+std |
|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
| A    | B      | C    | C    | C    | C    |
| D    | E      | F    | C    | C    | C    |

