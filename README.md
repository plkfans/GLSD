# GLSD
This is the Pytorch implementation of GLSD for remote sensing scene image classification.

# Requirements
Python 3.8, Pytorch 2.4, CUDA 12.4

# Usage
## Data preparation

## Training model

# Experimental results
All the experiments are implemented by Pytorch 2.4.1 Version in the computing environment of 1 × 24-GB NVIDIA GeForce RTX 4090 GPU. In order to obtain reliable experimental results, we randomly divided the dataset using the same training ratio on each dataset, repeated the experiment five times, and reported the mean and standard deviation of these results. The `train.log`
 and `model.pth` of each result are provided on [Github Releases](https://github.com).
## AID
20% Training:
| model | AID_20%_1 | AID_20%_2 | AID_20%_3 | AID_20%_4 | AID_20%_5 | mean+std |
|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
| ResNet18_va         | B      | C    | C    | C    | C    |
| ResNet18_kd         | B      | C    | C    | C    | C    |
| VGG11BN_va          | E      | F    | C    | C    | C    |
| VGG11BN_kd          | E      | F    | C    | C    | C    |
| WRN50_2_va          | E      | F    | C    | C    | C    |
| WRN50_2_kd          | E      | F    | C    | C    | C    |
| ShuffleNetV2×1.5_va | E      | F    | C    | C    | C    |
| ShuffleNetV2×1.5_kd | E      | F    | C    | C    | C    |

50% Training:
| model | AID_50%_1 | AID_50%_2 | AID_50%_3 | AID_50%_4 | AID_50%_5 | mean+std |
|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
| ResNet18_va         | B      | C    | C    | C    | C    |
| ResNet18_kd         | B      | C    | C    | C    | C    |
| VGG11BN_va          | E      | F    | C    | C    | C    |
| VGG11BN_kd          | E      | F    | C    | C    | C    |
| WRN50_2_va          | E      | F    | C    | C    | C    |
| WRN50_2_kd          | E      | F    | C    | C    | C    |
| ShuffleNetV2×1.5_va | E      | F    | C    | C    | C    |
| ShuffleNetV2×1.5_kd | E      | F    | C    | C    | C    |

## UCM
50% Training:
| model | UCM_50%_1 | UCM_50%_2 | UCM_50%_3 | UCM_50%_4 | UCM_50%_5 | mean+std |
|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
| ResNet18_va         | B      | C    | C    | C    | C    |
| ResNet18_kd         | B      | C    | C    | C    | C    |
| VGG11BN_va          | E      | F    | C    | C    | C    |
| VGG11BN_kd          | E      | F    | C    | C    | C    |
| WRN50_2_va          | E      | F    | C    | C    | C    |
| WRN50_2_kd          | E      | F    | C    | C    | C    |
| ShuffleNetV2×1.5_va | E      | F    | C    | C    | C    |
| ShuffleNetV2×1.5_kd | E      | F    | C    | C    | C    |

80% Training:
| model | UCM_80%_1 | UCM_80%_2 | UCM_80%_3 | UCM_80%_4 | UCM_80%_5 | mean+std |
|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
| ResNet18_va         | B      | C    | C    | C    | C    |
| ResNet18_kd         | B      | C    | C    | C    | C    |
| VGG11BN_va          | E      | F    | C    | C    | C    |
| VGG11BN_kd          | E      | F    | C    | C    | C    |
| WRN50_2_va          | E      | F    | C    | C    | C    |
| WRN50_2_kd          | E      | F    | C    | C    | C    |
| ShuffleNetV2×1.5_va | E      | F    | C    | C    | C    |
| ShuffleNetV2×1.5_kd | E      | F    | C    | C    | C    |



