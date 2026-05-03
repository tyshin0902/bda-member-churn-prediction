# BDA 학회원 이탈률 예측

회원 프로필, 활동, 참여 관련 데이터를 활용하여 BDA 학회원의 이탈 여부를 예측하는 머신러닝 프로젝트입니다.

## 개요

이 프로젝트는 BDA 학회원이 조직에서 이탈할 가능성이 있는지를 예측하는 것을 목표로 합니다.  
단순히 분류 모델을 만드는 것뿐만 아니라, 어떤 유형의 회원 정보가 이탈 위험을 파악하는 데 유용할 수 있는지도 함께 분석합니다.

프로젝트는 일반적인 머신러닝 workflow를 따릅니다.

1. 탐색적 데이터 분석
2. 데이터 전처리
3. 모델 학습
4. 하이퍼파라미터 튜닝
5. 모델 평가

## 문제 정의

학회원 이탈 예측은 이진 분류 문제입니다.

- **Target variable:** `withdrawal`
- **Positive class:** 학회원이 이탈함
- **Negative class:** 학회원이 이탈하지 않음

데이터셋에 클래스 불균형이 존재하기 때문에, 이 프로젝트에서는 정확도만 사용하지 않고 **F1 score**를 주요 평가 지표로 사용합니다.

## 데이터셋

원본 학습 데이터셋은 다음과 같이 구성되어 있습니다.

- **Train data:** 1,056 rows and 46 columns
- **Test data:** 788 rows and 45 columns

데이터셋에는 다음과 같은 학회원 관련 정보가 포함되어 있습니다.

- 학교 및 전공 정보
- 직장 여부
- 재등록 여부
- 이전 기수 참여 정보
- 프로젝트 선호도
- 투입 가능 시간
- 공모전 참여 여부
- 진로 또는 학습 관련 설문 응답

전처리 이후 최종 학습 데이터는 다음과 같이 구성되었습니다.

- **Processed features:** 24개
- **Target distribution:**
  - `withdrawal = 1`: 730명
  - `withdrawal = 0`: 326명

## 프로젝트 구조

```text
bda-member-churn-prediction/
├── data/                         # 원본 및 전처리된 데이터 파일
├── 01_EDA.ipynb                  # 탐색적 데이터 분석
├── 02_Preprocessing.ipynb        # 데이터 정리 및 feature 전처리
├── 03_Modeling.ipynb             # 모델 학습, 튜닝, 평가
├── 04_Additional_Analysis.ipynb  # 추가 실험 및 분석
├── requirements.txt              # 필요한 Python 패키지
└── README.md                     # 프로젝트 문서