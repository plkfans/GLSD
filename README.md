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
| ResNet18_va         | 93.15%      | 93.89%    | 93.73%    | 93.59%    | 92.90%    | 93.45±0.37
| ResNet18_kd         | 96.14%      | 96.34%    | 96.11%    | 96.06%    | 96.17%    | **96.16±0.10**(+2.71%)
| VGG11BN_va          | 92.33%      | 92.76%    | 93.17%    | 92.46%    | 92.59%    | 92.66±0.29
| VGG11BN_kd          | 97.06%      | 97.12%    | 97.16%    | 96.94%    | 96.88%    | **97.03±0.11**(+4.37%)
| WRN50_2_va          | 93.96%      | 93.80%    | 94.06%    | 94.21%    | 94.21%    | 94.05±0.16
| WRN50_2_kd          | 96.17%      | 96.51%    | 96.75%    | 96.64%    | 96.40%    | **96.49±0.20**(+2.44%)
| ShuffleNetV2×1.5_va | 91.91%      | 92.33%    | 92.79%    | 93.06%    | 92.70%    | 92.56±0.40
| ShuffleNetV2×1.5_kd | 96.09%      | 96.00%    | 95.89%    | 96.62%    | 96.29%    | **96.18±0.26**(+3.62%)

50% Training:
| model | AID_50%_1 | AID_50%_2 | AID_50%_3 | AID_50%_4 | AID_50%_5 | mean+std |
|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
| ResNet18_va         | 95.22%      | 95.72%    | 95.60%    | 95.36%    | 95.90%    | 95.56±0.24
| ResNet18_kd         | 97.56%      | 97.58%    | 97.80%    | 98.02%    | 97.92%    | **97.78±0.18**(+2.22%)
| VGG11BN_va          | 95.44%      | 95.42%    | 95.56%    | 95.42%    | 95.40%    | 95.45±0.06
| VGG11BN_kd          | 98.50%      | 98.58%    | 98.68%    | 98.48%    | 98.72%    | **98.59±0.10**(+3.14%)
| WRN50_2_va          | 96.00%      | 95.82%    | 96.04%    | 96.10%    | 96.50%    | 96.09±0.22
| WRN50_2_kd          | 97.84%      | 97.86%    | 98.00%    | 98.06%    | 98.26%    | **98.00±0.15**(+1.91%)
| ShuffleNetV2×1.5_va | 95.12%      | 95.34%    | 95.50%    | 94.94%    | 95.40%    | 95.26±0.20
| ShuffleNetV2×1.5_kd | 97.80%      | 97.52%    | 97.92%    | 97.84%    | 97.84%    | **97.78±0.14**(+2.52%)

## UCM
50% Training:
| model | UCM_50%_1 | UCM_50%_2 | UCM_50%_3 | UCM_50%_4 | UCM_50%_5 | mean+std |
|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
| ResNet18_va         | 97.24%      | 97.33%    | 98.19%    | 97.81%    | 97.24%    | 97.56±0.38
| ResNet18_kd         | 98.95%      | 98.86%    | 99.05%    | 98.76%    | 98.48%    | **98.82±0.20**(+1.26%)
| VGG11BN_va          | 96.57%      | 97.14%    | 96.38%    | 97.05%    | 96.57%    | 96.74±0.30
| VGG11BN_kd          | 99.05%      | 99.05%    | 99.43%    | 98.76%    | 98.76%    | **99.01±0.25**(+2.27%)
| WRN50_2_va          | 97.52%      | 98.29%    | 98.86%    | 97.90%    | 97.62%    | 98.04±0.49
| WRN50_2_kd          | 98.86%      | 99.24%    | 99.24%    | 98.67%    | 98.67%    | **98.94±0.26**(+0.90%)
| ShuffleNetV2×1.5_va | 97.24%      | 96.29%    | 97.62%    | 96.86%    | 97.24%    | 97.05±0.45
| ShuffleNetV2×1.5_kd | 98.48%      | 98.48%    | 99.24%    | 98.57%    | 98.86%    | **98.73±0.29**(+1.68%)

80% Training:
| model | UCM_80%_1 | UCM_80%_2 | UCM_80%_3 | UCM_80%_4 | UCM_80%_5 | mean+std |
|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
| ResNet18_va         | 99.29%      | 98.81%    | 99.29%    | 98.10%    | 98.57%    | 98.81±0.45
| ResNet18_kd         | 99.76%      | 99.52%    | 100.00%    | 99.05%    | 99.29%    | **99.52±0.34**(+0.71%)
| VGG11BN_va          | E      | F    | C    | C    | C    |
| VGG11BN_kd          | E      | F    | C    | C    | C    |
| WRN50_2_va          | E      | F    | C    | C    | C    |
| WRN50_2_kd          | E      | F    | C    | C    | C    |
| ShuffleNetV2×1.5_va | E      | F    | C    | C    | C    |
| ShuffleNetV2×1.5_kd | E      | F    | C    | C    | C    |

## RSSCN7
20% Training:
| model | RSSCN7_20%_1 | RSSCN7_20%_2 | RSSCN7_20%_3 | RSSCN7_20%_4 | RSSCN7_20%_5 | mean+std |
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
| model | RSSCN7_50%_1 | RSSCN7_50%_2 | RSSCN7_50%_3 | RSSCN7_50%_4 | RSSCN7_50%_5 | mean+std |
|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
| ResNet18_va         | B      | C    | C    | C    | C    |
| ResNet18_kd         | B      | C    | C    | C    | C    |
| VGG11BN_va          | E      | F    | C    | C    | C    |
| VGG11BN_kd          | E      | F    | C    | C    | C    |
| WRN50_2_va          | E      | F    | C    | C    | C    |
| WRN50_2_kd          | E      | F    | C    | C    | C    |
| ShuffleNetV2×1.5_va | E      | F    | C    | C    | C    |
| ShuffleNetV2×1.5_kd | E      | F    | C    | C    | C    |

## NWPU-RESISC45
10% Training:
| model | NWPU-RESISC45_10%_1 | NWPU-RESISC45_10%_2 | NWPU-RESISC45_10%_3 | NWPU-RESISC45_10%_4 | NWPU-RESISC45_10%_5 | mean+std |
|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
| ResNet18_va         | B      | C    | C    | C    | C    |
| ResNet18_kd         | B      | C    | C    | C    | C    |
| VGG11BN_va          | E      | F    | C    | C    | C    |
| VGG11BN_kd          | E      | F    | C    | C    | C    |
| WRN50_2_va          | E      | F    | C    | C    | C    |
| WRN50_2_kd          | E      | F    | C    | C    | C    |
| ShuffleNetV2×1.5_va | E      | F    | C    | C    | C    |
| ShuffleNetV2×1.5_kd | E      | F    | C    | C    | C    |

20% Training:
| model | NWPU-RESISC45_20%_1 | NWPU-RESISC45_20%_2 | NWPU-RESISC45_20%_3 | NWPU-RESISC45_20%_4 | NWPU-RESISC45_20%_5 | mean+std |
|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
| ResNet18_va         | B      | C    | C    | C    | C    |
| ResNet18_kd         | B      | C    | C    | C    | C    |
| VGG11BN_va          | E      | F    | C    | C    | C    |
| VGG11BN_kd          | E      | F    | C    | C    | C    |
| WRN50_2_va          | E      | F    | C    | C    | C    |
| WRN50_2_kd          | E      | F    | C    | C    | C    |
| ShuffleNetV2×1.5_va | E      | F    | C    | C    | C    |
| ShuffleNetV2×1.5_kd | E      | F    | C    | C    | C    |



