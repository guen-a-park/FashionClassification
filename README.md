# Classification of k-fashion images

(2022.05.02~2022.06.10)

22-1학기  "패턴인식과머신러닝" 과목의 팀프로젝트입니다.

## Purpose  

본 프로젝트의 목적은 fashion image를 입력받아 자동으로 Resort / Retro / Sporty 로 분류하는 Convolutional Neural  Network (CNN)을 개발하는 것으로 해당 프로젝트에서는 AlexNet, VGGNet, GoogleNet, ResNet, Densenet의 모델 구조를 참고하여 학습을 진행하였다.

## Train Data

Train data 7200장 Validation data 1800으로 training을 진행했고 Data augmentation을 이용해 각 Train data를 rotate과 horizontal flip의  방법을 랜덤하게 적용해 14400장으로 늘려주었다.

```bash
├── Train
│ ├── Resort
│ ├── Retro
│ └── Sporty
└── Validation
├── Resort
├── Retro
└── Sporty
```

## Result

최종모델은 Googlenet에서 batch size를 64로 설정한 모델로 선정하였다. 따라서 구글넷에서 필요한 224x224의 fashion image를 입력으로 받고 class를 예측할 수 있도록 코드를 작성하였다. 이때의 block diagram과 accurary 및 loss plot은 아래와 같다. 

![image](https://user-images.githubusercontent.com/77844152/181900158-37a48368-b703-43b9-b45f-596c71d15c5f.png)

|                           Accuracy                           |                             Loss                             |
| :----------------------------------------------------------: | :----------------------------------------------------------: |
| ![image](https://user-images.githubusercontent.com/77844152/181899360-8c2c8df8-2185-48a9-9362-f42605ff5d34.png) | ![image](https://user-images.githubusercontent.com/77844152/181899488-c0bcde93-0a80-4542-bb5d-7dda0dadb684.png) |

아래 표는 각 모델에 대한 세부적인 hyper parameter와 train accuracy로 자세한 결과는 보고서를 통해 확인할 수 있다. [[link]](https://github.com/guen-a-park/FashionClassification/blob/main/TeamB_report.pdf)

<img src="https://user-images.githubusercontent.com/77844152/181899046-f657516d-bfd9-4a1b-a207-4e1aa07adb2d.PNG" alt="result" style="zoom:80%;" />

## Test Score

1200개 test 파일에 대한 classification 결과는 76.08%의 accuracy로 13개 팀 중  2위

## Structure

```bash
FashionClassification
├── README.md
├── codes
│   ├───Alexnet_batch128.ipynb
│   ├───Densenet_batch64.ipynb
│   ├───Resnet34_batch128.ipynb
│   └───VGGNet_layer10.ipynb
├── Train_FashionClassification_TeamB.ipynb
├── Test_FashionClassification_TeamB.ipynb
├── TeamB_report.pdf
└── Model_TeamB
 
```

## Cotributors

Team B : 김나윤,박근아,이하은,정민주

## Code Reference

- [Data Augmentation](https://hipolarbear.tistory.com/19)

- [Classification report](https://gaussian37.github.io/ml-concept-ml-evaluation/#accuracy-1)
- Model
  - [Vggnet](https://minjoos.tistory.com/6)
  - [Densenet](https://deep-learning-study.tistory.com/545)
  - [Resnet](https://pseudo-lab.github.io/pytorch-guide/docs/ch03-1.html)
  - [Alexnet](https://medium.com/analytics-vidhya/alexnet-a-simple-implementation-using-pytorch-30c14e8b6db2)
  - [Googlenet](https://deep-learning-study.tistory.com/523)
