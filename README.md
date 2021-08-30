# YOLOv1_implement_using_Tensorflow_or_Pytorch

<img width="618" alt="YOLO_architecture" src="https://user-images.githubusercontent.com/50979281/130927332-1aefef43-c67e-48db-98fe-68cd0a1ad629.png">

This repository consist of YOLO implement code for CUAI 2021 summer conference. We made these codes using Tensorflow or Pyrotch.

YOLO v1 : https://arxiv.org/abs/1506.02640

## Members
Minki Kang(School of Computer Science and Engineering, Chung-Ang University)
<br>
[Minkyu Kim](https://github.com/MinkyuKim26)(School of Electrical and Electronics Engineering)
<br>
Taeyun Kim(School of Computer Science and Engineering, Chung-Ang University)
<br>
Seungyeon Lee(School of Computer Science and Engineering, Chung-Ang University)

## Short paper
작성중!

## How to implement?

### Using Tensorlfow - 강민기, 김민규

 For easy implementation, we use VGG or DenseNet which are made in Tensorflow. Training stragy

김민규 : 구현 난이도를 이유로 Backbone을 VGG-16으로 변경하고 데이터 증강을 구현하지 않았습니다. 훈련 방법은 논문에 나온 값(배치 사이즈, 에포크 등)을 그대로 사용했고 매 에포크마다 검증 로스(검증용 데이터셋에 대한 로스, Verification Loss)가 줄어들면 저장하여 검증 로스가 가장 낮은 모델을 최종 훈련 모델로 선택하였습니다. 
테스트 결과, 훈련용 데이터셋에 오버피팅되어 테스트용 데이터셋에서는 좋지 못한 성능을 보여줬습니다. 데이터 증강을 구현하지 못한 것이 오버피팅의 주요 원인이라 생각됩니다.

### Using Pytorch - 김태윤, 이승연

김태윤 + 이승연 : 파이토치로 구현된 DarkNet을 backbone으로 사용했습니다. 

## 구현 모델 테스트 방법

강민기 : 

김민규 : Minkyu Kim폴더에 있는 YOLO_test.ipynb와 구글 드라이브(https://drive.google.com/file/d/18wl62z2sU3O6NUl45K7iYSzWnGlpUYzV/view?usp=sharing)에 있는 yolo-minkyuKim.h5를 다운받은 뒤 두 파일을 같은 위치에 놓고 YOLO_test.ipynb에 있는 블록을 위에서부터 차례대로 실행시키시거나  load_YOLO()에 있는 YOLO.load_weights()의 파일 경로를 yolo-minkyuKim.h5의 경로에 맞게 수정하신 뒤 위에서부터 차례대로 실행시키시면 됩니다.

김태윤 + 이승연 : 


