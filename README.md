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
| model | data1 | data2 | data3 | data4 | data5 | mean+std |
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
| model | data1 | data2 | data3 | data4 | data5 | mean+std |
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
| model | data1 | data2 | data3 | data4 | data5 | mean+std |
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
| model | data1 | data2 | data3 | data4 | data5 | mean+std |
|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
| ResNet18_va         | 99.29%      | 98.81%    | 99.29%    | 98.10%    | 98.57%    | 98.81±0.45
| ResNet18_kd         | 99.76%      | 99.52%    | 100.00%    | 99.05%    | 99.29%    | **99.52±0.34**(+0.71%)
| VGG11BN_va          | 98.57%      | 96.90%    | 98.10%    | 98.33%    | 97.86%    | 97.95±0.58
| VGG11BN_kd          | 99.76%      | 99.52%    | 100.00%    | 99.29%    | 99.29%    | **99.57±0.28**(+1.62%)
| WRN50_2_va          | 99.29%      | 98.10%    | 99.52%    | 98.57%    | 98.81%    | 98.86±0.51
| WRN50_2_kd          | 99.76%      | 99.29%    | 99.52%    | 99.52%    | 99.52%    | **99.52±0.15**(+0.66%)
| ShuffleNetV2×1.5_va | 98.81%      | 97.86%    | 99.05%    | 97.14%    | 97.38%    | 98.05±0.76
| ShuffleNetV2×1.5_kd | 99.52%      | 99.05%    | 99.52%    | 98.81%    | 98.81%    | **99.14±0.32**(+1.09%)

## RSSCN7
20% Training:
| model | data1 | data2 | data3 | data4 | data5 | mean+std |
|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
| ResNet18_va         | 91.65%      | 92.19%    | 90.62%    | 91.03%    | 91.56%    | 91.41±0.54
| ResNet18_kd         | 95.94%      | 96.47%    | 95.62%    | 96.43%    | 96.21%    | **96.13±0.32**(+4.72%)
| VGG11BN_va          | 94.33%      | 93.35%    | 92.63%    | 93.66%    | 93.71%    | 93.54±0.55
| VGG11BN_kd          | 97.41%      | 98.17%    | 96.88%    | 97.77%    | 97.37%    | **97.52±0.43**(+3.98%)
| WRN50_2_va          | 93.88%      | 92.59%    | 91.83%    | 93.12%    | 92.81%    | 92.85±0.67
| WRN50_2_kd          | 96.25%      | 96.83%    | 95.85%    | 96.25%    | 96.79%    | **96.39±0.37**(+3.54%)
| ShuffleNetV2×1.5_va | 92.28%      | 92.10%    | 90.31%    | 91.79%    | 90.94%    | 91.48±0.75
| ShuffleNetV2×1.5_kd | 96.56%      | 96.88%    | 96.47%    | 97.86%    | 96.74%    | **96.90±0.50**(+5.42%)

50% Training:
| model | data1 | data2 | data3 | data4 | data5 | mean+std |
|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
| ResNet18_va         | 95.21%      | 94.43%    | 95.21%    | 94.79%    | 95.29%    | 94.99±0.33
| ResNet18_kd         | 97.71%      | 98.00%    | 98.00%    | 98.14%    | 98.50%    | **98.07±0.26**(+3.08%)
| VGG11BN_va          | 96.00%      | 95.50%    | 96.71%    | 95.86%    | 96.79%    | 96.17±0.50
| VGG11BN_kd          | 98.86%      | 98.86%    | 99.36%    | 98.86%    | 99.21%    | **99.03±0.21**(+2.86%)
| WRN50_2_va          | 96.21%      | 95.29%    | 95.79%    | 96.21%    | 96.21%    | 95.94±0.36
| WRN50_2_kd          | 98.21%      | 97.93%    | 97.93%    | 98.21%    | 98.57%    | **98.17±0.24**(+2.23%)
| ShuffleNetV2×1.5_va | 94.36%      | 94.29%    | 94.50%    | 94.50%    | 95.57%    | 94.64±0.47
| ShuffleNetV2×1.5_kd | 99.14%      | 98.71%    | 99.21%    | 98.79%    | 99.14%    | **99.00±0.21**(+4.36%)

## NWPU-RESISC45
10% Training:
| model | data1 | data2 | data3 | data4 | data5 | mean+std |
|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
| ResNet18_va         | 89.29%      | 88.69%    | 88.74%    | 89.33%    | 88.54%    | 88.92±0.33
| ResNet18_kd         | 93.96%      | 93.33%    | 93.83%    | 93.83%    | 93.30%    | **93.65±0.28**(+4.73%)
| VGG11BN_va          | 87.22%      | 87.31%    | 86.73%    | 87.62%    | 86.85%    | 87.15±0.32
| VGG11BN_kd          | 94.46%      | 94.19%    | 94.28%    | 94.34%    | 93.96%    | **94.25±0.17**(+7.10%)
| WRN50_2_va          | 90.74%      | 90.99%    | 90.37%    | 91.10%    | 90.72%    | 90.78±0.25
| WRN50_2_kd          | 94.06%      | 94.38%    | 94.07%    | 94.44%    | 93.73%    | **94.14±0.26**(+3.36%)
| ShuffleNetV2×1.5_va | 88.70%      | 88.34%    | 88.23%    | 87.88%    | 88.11%    | 88.25±0.27
| ShuffleNetV2×1.5_kd | 93.60%      | 92.71%    | 93.69%    | 93.80%    | 93.23%    | **93.41±0.40**(+5.16%)

20% Training:
| model | data1 | data2 | data3 | data4 | data5 | mean+std |
|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
| ResNet18_va         | 91.93%      | 91.88%    | 91.97%    | 91.71%    | 91.85%    | 91.87±0.09
| ResNet18_kd         | 95.73%      | 96.06%    | 95.82%    | 95.85%    | 95.84%    | **95.86±0.11**(+3.99%)
| VGG11BN_va          | 90.96%      | 90.85%    | 90.94%    | 90.64%    | 90.79%    | 90.84±0.12
| VGG11BN_kd          | 96.42%      | 96.72%    | 96.54%    | 96.51%    | 96.60%    | **96.56±0.10**(+5.72%)
| WRN50_2_va          | 93.46%      | 93.54%    | 93.67%    | 93.57%    | 93.56%    | 93.56±0.07
| WRN50_2_kd          | 96.04%      | 96.08%    | 96.07%    | 96.10%    | 95.93%    | **96.04±0.06**(+2.48%)
| ShuffleNetV2×1.5_va | 91.46%      | 91.32%    | 91.39%    | 91.40%    | 91.42%    | 91.40±0.05
| ShuffleNetV2×1.5_kd | 96.23%      | 95.29%    | 95.56%    | 95.37%    | 95.52%    | **95.59±0.33**(+4.19%)

## VGG11 & Efficientnet_b3
| datasets | data1 | data2 | data3 | data4 | data5 | mean+std |
|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
| AID_20%_va           | 92.33%      | 92.76%    | 93.17%    | 92.46%    | 92.59%    | 92.66±0.29
| AID_20%_kd           | 97.36%      | 97.76%    | 97.61%    | 97.52%    | 97.88%    | **97.63±0.18**(+4.97%)
| AID_50%_va           | 95.44%      | 95.42%    | 95.56%    | 95.42%    | 95.40%    | 95.45±0.06
| AID_50%_kd           | 98.92%      | 99.10%    | 99.10%    | 98.86%    | 99.14%    | **99.02±0.11**(+3.57%)
| UCM_50%_va           | 96.57%      | 97.14%    | 96.38%    | 97.05%    | 96.57%    | 96.74±0.30
| UCM_50%_kd           | 99.14%      | 99.33%    | 99.43%    | 99.14%    | 99.43%    | **99.29±0.13**(+2.55%)
| UCM_80%_va           | 98.57%      | 96.90%    | 98.10%    | 98.33%    | 97.86%    | 97.95±0.58
| UCM_80%_kd           | 99.76%      | 99.29%    | 100.0%    | 99.52%    | 99.76%    | **99.67±0.24**(+1.72%)
| RSSCN7_20%_va        | 94.33%      | 93.35%    | 92.63%    | 93.66%    | 93.71%    | 93.54±0.55
| RSSCN7_20%_kd        | 97.95%      | 98.12%    | 97.77%    | 97.46%    | 97.46%    | **97.75±0.26**(+4.21%)
| RSSCN7_50%_va        | 96.00%      | 95.50%    | 96.71%    | 95.86%    | 96.79%    | 96.17±0.50
| RSSCN7_50%_kd        | 99.21%      | 99.29%    | 99.14%    | 99.14%    | 99.29%    | **99.21±0.07**(+3.04%)
| NWPU-RESISC45_10%_va | 87.22%      | 87.31%    | 86.73%    | 87.62%    | 86.85%    | 87.15±0.32
| NWPU-RESISC45_10%_kd | 95.49%      | 95.17%    | 95.47%    | 95.41%    | 95.20%    | **95.35±0.14**(+8.20%)
| NWPU-RESISC45_20%_va | 90.96%      | 90.85%    | 90.94%    | 90.64%    | 90.79%    | 90.84±0.12
| NWPU-RESISC45_20%_kd | 97.31%      | 97.35%    | 97.29%    | 97.30%    | 97.30%    | **97.31±0.02**(+6.47%)

## Efficientnet_b3 & Efficientnet_b3
| datasets | data1 | data2 | data3 | data4 | data5 | mean+std |
|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
| AID_20%_va           | 95.60%      | 95.66%    | 95.86%    | 95.76%    | 95.73%    | 95.72±0.09
| AID_20%_kd           | 97.52%      | 97.76%    | 97.95%    | 97.78%    | 97.56%    | **97.71±0.16**(+1.99%)
| AID_50%_va           | 97.22%      | 97.30%    | 97.60%    | 97.46%    | 97.18%    | 97.35±0.16
| AID_50%_kd           | 98.96%      | 99.10%    | 98.74%    | 98.98%    | 99.28%    | **99.01±0.18**(+1.66%)
| NWPU-RESISC45_10%_va | 92.43%      | 92.09%    | 92.26%    | 92.43%    | 92.11%    | 92.26±0.15
| NWPU-RESISC45_10%_kd | 96.05%      | 95.77%    | 95.58%    | 95.98%    | 95.47%    | **95.77±0.22**(+3.51%)
| NWPU-RESISC45_20%_va | 94.65%      | 94.49%    | 94.45%    | 94.62%    | 94.42%    | 94.53±0.09
| NWPU-RESISC45_20%_kd | 97.60%      | 97.37%    | 97.42%    | 97.51%    | 97.37%    | **97.45±0.09**(+2.92%)




