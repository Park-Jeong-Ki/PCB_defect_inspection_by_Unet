# PCB_defect_inspection_by_Unet

colab 예시

[https://colab.research.google.com/drive/1DdOeQ74GNgFjGnblKRHSKTfhzQAeBJO5?usp=sharing]

---

## 프로젝트 개요
| PCB 결함을 검출하는 CNN 모델을 만들어보자!


사람 눈으로는 찾지 못하는 PCB 기판의 결함을 딥러닝을 활용하여 검출해 냈습니다. 의료 영상에서 자주 쓰이는 Unet 모델을 가져와서 PCB 기판 데이터를 넣어서 모델을 만들어 봤습니다. 'Unet 모델이 의료 영상 뿐만 아니라 회로 기판 이미지 에서도 성능이 좋을 것이다' 라는 가설을 세우고 프로젝트를 진행해 봤습니다.

## 프로젝트 목표

| Unet model로 PCB 결함 찾는 모델 구현

| 가설 검증

| 찍는 확률 보다 높은 정확도 모델 구현, 다양한 조건의 모델 실험

## 결론

| 검증 데이터 정확도 91.3%의 PCB 결함 검출 모델을 구현했어요!

6종이나 되는 결함의 종류 또한 분류해 내면서 PCB 결함을 검출해 내는 모델을 구현했습니다. 데이터 크기에 비해 모델이 컸던 Unet 모델을 작게 만들어 mini Unet 모델로 만들어서 성능을 향상 시켰습니다. 앞서 설정한 가설도 실험을 통해서 Unet 모델이 회로 기판 결함 검출에도 효과적이라는 것을 검증했습니다.

추후 이미지 데이터를 반도체 칩 결함 이미지, 미세 회로 이미지로 바꿔서 학습 시켜도 유용하게 쓰일 수 있을 것 같습니다!

---

## Train/Validatation Data
케글에 공유된 PCB 데이터 사용: https://www.kaggle.com/yidazhang07/bridge-cracks-image

## Unet Model

![image](https://user-images.githubusercontent.com/71398226/133598612-6f6cafc2-2245-4e93-a9db-afced6d1d3e8.png)

## Mini Unet

![image](https://user-images.githubusercontent.com/71398226/133598662-f98a1ddf-f532-410d-a364-1ab4e423ebe3.png)

---


## Best Model Parameter
- Mini Unet model
- epoch 1000 
- batch size 100
- BatchNormalization 사용
- adam 사용
- SparseCategoricalCrossentropy 사용

## Best Model Result

![image](https://user-images.githubusercontent.com/71398226/133598487-8d4d9e99-f5bc-4340-897a-c620bcad3a53.png)

## Test Data Result

![image](https://user-images.githubusercontent.com/71398226/133598521-4270928c-cbee-4aaf-8f15-7487c462bbad.png)


