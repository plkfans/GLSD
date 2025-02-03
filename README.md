![image](https://github.com/user-attachments/assets/051ba865-58b5-4429-b8bd-39dca2a591fc)# GLSD
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
| ResNet18_va         | 93.15%      | 93.89%    | 93.73%    | 93.59%    | 92.90%    | 93.45±0.37
| ResNet18_kd         | 96.14%      | 96.34%    | 96.11%    | 96.06%    | 96.17%    | **96.16±0.10**(+2.71%)
| VGG11BN_va          | 92.33%      | 92.76%    | 93.17%    | 92.46%    | 92.59%    | 92.66±0.29
| VGG11BN_kd          | 97.06%      | 97.12%    | 97.16%    | 96.94%    | 96.88%    | **97.03±0.11**(+4.37%)
| WRN50_2_va          | 93.96%      | 93.80%    | 94.06%    | 94.21%    | 94.21%    | 94.05±0.16
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



