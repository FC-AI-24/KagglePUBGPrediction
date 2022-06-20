# PUBG Finish Placement Prediction (Kernels Only)
## 배경
- Battle Royale-style video games으로 총 100명의 플레이어가 게임의 참여하며 
최후의 1인이 남을 때 까지 다른 플레이어를 제거하는 게임입니다.
<img width="650" src="https://storage.googleapis.com/kaggle-media/competitions/PUBG/PUBG%20Inlay.jpg">

[대회 링크](https://www.kaggle.com/competitions/pubg-finish-placement-prediction)

## 목표
- "winPlacePerc" 0~1까지를 예측 모델링
- 100명 중 몇 번째까지 살아남았는지 백분율 예측 목표

## 팀원
- 최진수, 박찬샘, 최선우, 양진호, 심승우

## DataLeakage
- 머신러닝 학습을 목적으로 대회에 참여하였기 때문에 Dataleakage 문제가 있는 "winPlace" 컬럼에 대해서 모델학습을 진행하지 않았습니다.

[DataLeakage 관련 토론](https://www.kaggle.com/competitions/pubg-finish-placement-prediction/discussion/79161)

## 파일 설명
BaseModelScore.ipynb
pubg_02.EDA.ipynb
Modeling.ipynb

## score

모델 성능 비교
|Model| MAE |
|---|-------:|
|BaseModel| 0.090|
|FinalModel| 0.066|