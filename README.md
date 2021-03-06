# MSDS19036_COVID19_DLSpring2020
This repository contains code and results for COVID-19 classification assignment by Deep Learning Spring 2020 course offered at Information Technology University, Lahore, Pakistan. This assignment is only for learning purposes and is not intended to be used for clinical purposes

# Assignment Part 2 (Focal Loss)
#### _MultiLabel MultiClass Classification_
## Results
![Results](/images/Results.PNG)

![Class Wise Accuracy](/images/class-wise-accuracy.PNG)

## Dataset
Dataset contain Total of 15000 X-Ray images from 2 classes.

Download dataset: https://drive.google.com/open?id=1-FzZhQO9oHIT9SNOWYoKsuz7fe447vtR <br />
For Zip File:     https://drive.google.com/open?id=1-HQQciKYfwAO3oH7ci6zhg45DduvkpnK

|Class|Training Set|Validation Set|Test Set|
|:---:|   :---:    |     :---:    | :---:  |
|Infected | 4919 | 615 | 615 |
|Normal   | 7081 | 885 | 885 |

## Pretrained weights
https://drive.google.com/open?id=1lNENcohvA9cunyh1GcPmZ1fqRiuzfSOW
</br>
## Testing:

#### Best Classified Images

![Best Classified (VGG16)](/images/T1-Image-VGG-Best-1.PNG)
![Best Classified (RESNET18)](/images/T1-Image-Resnet-Best-1.PNG)

#### Worst Classified Images

![Worst Classified (VGG16)](/images/T1-Image-VGG-Worst-1.PNG)
![Worst Classified (RESNET18)](/images/T1-Image-Resnet-Worst-1.PNG)
</br>

## Results /  Accuracy Scores:

| Backbone | Frozen Layers| Epochs | Training Accuracy | F1 Score (Training) | Testing Set Accuracy | F1 Score (Testing) |
|----------|--------------|  :---:  |       :---:       |        :---:        |       :---:         |       :---:        |
| VGG16    | All Layers except FC   | 20 | 83%          | 0.81                | 80%                 |         0.75       |
| RESNET18 | All Layers except FC   | 20 | 89%          | 0.88                | 85%                 |         0.88       |
| VGG16    | Last 2 conv. and FC Layers | 20 | 99%      | 0.99                | 89%                 |         0.87       |
| VGG16    | None                   | 20 | 99%          | 0.98                | 90%                 |         0.88       |
| RESNET18 | (Layer 4) CNNs and FC Layers | 20 | 99%    | 0.96                | 88%                 |         0.86       |
| RESNET18 | None                   | 20 | 99%          | 0.99                | 85%                 |         0.81       |
