# Notebooks

이 폴더는 MetroGuard-AI 프로젝트의 전체 분석 및 모델링 과정을 단계별로 정리한 Jupyter Notebook 파일들로 구성됩니다.

---

## 1. preprocessing_final.ipynb

프로젝트 전체 데이터 전처리를 수행하는 노트북입니다.

주요 내용:
- 데이터 정제 및 결측치 처리
- 역명 통합 및 변수 정규화
- 시간대(time_group) 생성
- 혼잡·유입·구조·환승 데이터 통합
- 사고 데이터 병합
- 최종 분석용 데이터셋 생성

산출물:
- df_final_all_preprocessed.csv
- df_final_struct_preprocessed.csv

---

## 2. Logistic_Regression_analysis.ipynb

Logistic Regression 기반 사고 예측 모델 분석 노트북입니다.

주요 내용:
- 사고 발생 여부 이진 분류
- 기본 베이스라인 모델 성능 평가
- Accuracy, Precision, Recall, F1-score 분석
- Confusion Matrix 확인

활용 목적:
- 전통 통계 기반 분류 모델과의 비교

---

## 3. RandomForest_analysis.ipynb

Random Forest 기반 사고 위험 분석 노트북입니다.

주요 내용:
- 앙상블 기반 사고 예측
- 변수 중요도(Feature Importance) 분석
- 모델 성능 비교
- 주요 위험 변수 확인

활용 목적:
- 비선형 변수 관계 분석
- 중요 변수 탐색

---

## 4. XGBClassifier_analysis.ipynb

XGBoost Classifier 기반 사고 발생 예측 모델 노트북입니다.

주요 내용:
- 사고 발생 여부 분류
- Risk Score 산출
- Feature Importance 분석
- 위험 유형 분류
- 주요 위험 원인 도출
- 맞춤형 안전 대응 전략 생성

활용 목적:
- 최종 핵심 위험도 모델 구축

---

## 5. XGBRegressor_analysis.ipynb

XGBoost Regressor 기반 위험도 회귀 분석 노트북입니다.

주요 내용:
- 사고 위험도 연속값 예측
- 회귀 기반 위험도 모델링
- RMSE / MAE 성능 평가
- 위험도 분포 분석

활용 목적:
- 연속형 위험도 예측 성능 확인

---

## 6. metroguard_decision_system.ipynb

MetroGuard-AI 정책 의사결정 지원 시스템 노트북입니다.

주요 내용:
- 위험 유형 자동 분류
- 주요 위험 요인 기여도 계산
- What-if 정책 민감도 분석
- 위험 완화 시나리오 시뮬레이션
- 맞춤형 대응 전략 추천

활용 목적:
- 정책 의사결정 지원
- 안전 대응 전략 자동 제안

---

## 7. metroguard_query_system.ipynb

사용자 질의 기반 위험 조회 시스템 노트북입니다.

주요 내용:
- 역명·호선·시간대 기반 위험 조회
- 위험 점수 출력
- 주요 위험 원인 설명
- 추천 대응 전략 제공

활용 목적:
- 실사용자 중심 위험 조회 인터페이스 구현

---

## 8. risk_map_visualization.ipynb

서울 지하철 위험도 지도 시각화 노트북입니다.

주요 내용:
- 역 위치 좌표 매핑
- 위험도 기반 지도 시각화
- 고위험 역 Highlight
- 시간대별 위험도 시각화
- 인터랙티브 지도 구성

활용 목적:
- 위험 지역 직관적 시각화
- 정책 및 현장 대응 지원

---

## 전체 분석 흐름

Preprocessing  
→ Baseline Modeling  
→ XGBoost 기반 위험도 모델링  
→ 위험 원인 분석  
→ 정책 의사결정 지원 시스템  
→ 위험도 조회 시스템  
→ 지도 시각화

---

## 핵심 기술 스택

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Matplotlib
- Seaborn
- Folium
- GeoPandas

---

## 프로젝트 목표

MetroGuard-AI는 서울시 지하철 승강장의 사고 위험을 시간대별·역별로 동적으로 분석하고, 단순 위험 예측을 넘어 위험 원인 해석 및 맞춤형 안전 대응 전략까지 제공하는 AI 기반 도시 안전 의사결정 지원 시스템 구축을 목표로 합니다.
