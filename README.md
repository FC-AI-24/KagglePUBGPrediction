# PUBG Finish Placement Prediction (Kernels Only)
## 배경
- Battle Royale-style video games으로 총 100명의 플레이어가 게임의 참여하며   
최후의 1인이 남을 때 까지 다른 플레이어를 제거하는 게임입니다.

<img width="650" src="https://storage.googleapis.com/kaggle-media/competitions/PUBG/PUBG%20Inlay.jpg">

[Kaggle 링크](https://www.kaggle.com/competitions/pubg-finish-placement-prediction)

## 목표
- "winPlacePerc" 0~1 값 회귀 예측 
- "winPlacePerc": 100명 중 몇 번째까지 살아남았는지 백분율 순위

## 팀원
- 최진수, 박찬샘, 최선우, 양진호, 심승우

## DataLeakage
- 머신러닝 학습 목적으로 대회에 참여하였기 때문에 Dataleakage 문제의 "winPlace"    
컬럼에 대해서 모델학습을 진행하지 않았습니다.

[DataLeakage 관련 토론](https://www.kaggle.com/competitions/pubg-finish-placement-prediction/discussion/79161)

## 파일 설명
** BaseModelScore.ipynb
- 성능 비교를 위한 자체 BaseModel 제작
- numeric column 데이터 XGBoost CrossValidation 학습 진행
- score 0.090

** pubg_02.EDA.ipynb
- EDA, 전처리, FeatureEngineering 작업 진행

** Modeling.ipynb
- 모델 학습하여 상위 3개 모델 select
- Voting Regression 학습 진행


## 모델 성능 비교

|Model| MAE |
|---|-------:|
|BaseModel| 0.090|
|VotingRegressor| 0.066|