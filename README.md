## Towards Principled Design of Deep Convolutional Networks: Introducing SimpNet

This repository contains the architectures, pretrained models, logs, etc pertaining to the SimpNet Paper (Towards Principled Design of Deep Convolutional Networks: Introducing SimpNet) : https://arxiv.org/abs/1802.06205 


SimpNet architecture is the successor to the the successful SimpleNet architecture. It is based on a series of design principles which allowed the architecture to become vastly superior to its precessor (SimpleNet) and also outperforming deeper and more complex architectures, such as Wide Residual Networks, ResNet, Fmax, etc on a series of highly compatative benchmark datasets such as CIFAR10/100, SVHN and MNIST). 

Note: The files are being uploaded...


## Results Overview :

#### Top CIFAR10/100 results:

| **Method**              | **\#Params** |  **CIFAR10**  | **CIFAR100** |
| :---------------------- | :----------: | :-----------: | :----------: |
| VGGNet(16L) /Enhanced   |     138m     | 91.4 / 92.45  |      \-      |
| ResNet-110L / 1202L  \* |  1.7/10.2m   | 93.57 / 92.07 | 74.84/72.18  |
| SD-110L / 1202L         |  1.7/10.2m   | 94.77 / 95.09 |  75.42 / -   |
| WRN-(16/8)/(28/10)      |    11/36m    | 95.19 / 95.83 |  77.11/79.5  |
| DenseNet                |    27.2m     |     96.26     |    80.75     |
| Highway Network         |     N/A      |     92.40     |    67.76     |
| FitNet                  |      1M      |     91.61     |    64.96     |
| FMP\* (1 tests)         |     12M      |     95.50     |    73.61     |
| Max-out(k=2)            |      6M      |     90.62     |    65.46     |
| Network in Network      |      1M      |     91.19     |    64.32     |
| DSN                     |      1M      |     92.03     |    65.43     |
| Max-out NIN             |      \-      |     93.25     |    71.14     |
| LSUV                    |     N/A      |     94.16     |     N/A      |
| **SimpNet**                 |    **5.48M**     |  **95.49/95.56**  |    **78.08**     |
| **SimpNet**                 |    **8.9M**    |     **95.89**     |    **79.17**     |


#### Comparisons of performance on SVHN:

| **Method**                   | **Error rate** |
| :--------------------------- | :------------: |
| Network in Network           |      2.35      |
| Deeply Supervised Net        |      1.92      |
| ResNet (reported by  (2016)) |      2.01      |
| ResNet with Stochastic Depth |      1.75      |
| DenseNet                     |   1.79-1.59    |
| Wide ResNet                  |   2.08-1.64    |
| **SimpNet**                  |    **1.648**  |

* The slim version achieves 1.95% error rate.

#### MNIST results:

| **Method**                   | **Error rate** |
| :--------------------------- | :------------: |
| Batch-normalized Max-out NIN |     0.24%      |
| Max-out network (k=2)        |     0.45%      |
| Network In Network           |     0.45%      |
| Deeply Supervised Network    |     0.39%      |
| RCNN-96                      |     0.31%      |
| **SimpNet**                      |     **0.25%**      |

* The slim version achives 99.73% accuracy.


#### Slim Version Results on CIFAR10/100 : 

| Model                                        |    Param    |    CIFAR10    |   CIFAR100    |
| :------------------------------------------- | :---------: | :-----------: | :-----------: |
| **SimpNet**                                  |**300K - 600K**| **93.25 - 94.03** | **68.47 - 71.74** |
| Maxout                                       |     6M      |     90.62     |     65.46     |
| DSN                                          |     1M      |     92.03     |     65.43     |
| ALLCNN                                       |    1.3M     |     92.75     |     66.29     |
| dasNet                                       |     6M      |     90.78     |     66.22     |
| ResNet  <span>(Depth32, tested by us)</span> |    475K     |     93.22     |  67.37-68.95  |
| WRN                                          |    600K     |     93.15     |     69.11     |
| NIN                                          |     1M      |     91.19     |       —       |



