# telecom_churn
팀 프로젝트-통신사 고객 이탈 예측 프로젝트
# 프로젝트 문제 정의 및 목표


<details>
<summary>📊 Data Card</summary>

| **Attribute**   | **Details**                                |
| --------------- | ------------------------------------------ |
| **Dataset Name**| Telco Customer Churn                       |
| **Source**      | Kaggle                                     |
| **Instances**   | 7,043 customers                            |
| **Features**    | 21 columns (20 features + 1 target)        |
| **Target**      | Churn (Yes/No)                             |

### Feature Description

| Feature             | Type     | Description                                            |
| ------------------- | -------- | ------------------------------------------------------ |
| customerID          | String   | 고객 식별자                                            |
| gender              | String   | 성별 (Male/Female)                                     |
| SeniorCitizen       | Integer  | 시니어 여부 (0: No, 1: Yes)                            |
| Partner             | String   | 배우자 여부 (Yes/No)                                   |
| Dependents          | String   | 부양가족 여부 (Yes/No)                                 |
| tenure              | Integer  | 서비스 이용 개월 수                                     |
| PhoneService        | String   | 전화 서비스 가입 여부 (Yes/No)                         |
| MultipleLines       | String   | 부가 전화선 여부 (Yes/No/No phone service)             |
| InternetService     | String   | 인터넷 서비스 유형 (DSL/Fiber optic/No)                |
| OnlineSecurity      | String   | 온라인 보안 서비스 가입 여부 (Yes/No/No internet service) |
| OnlineBackup        | String   | 온라인 백업 서비스 가입 여부 (Yes/No/No internet service) |
| DeviceProtection    | String   | 디바이스 보호 서비스 가입 여부 (Yes/No/No internet service) |
| TechSupport         | String   | 기술 지원 서비스 가입 여부 (Yes/No/No internet service) |
| StreamingTV         | String   | TV 스트리밍 서비스 가입 여부 (Yes/No/No internet service) |
| StreamingMovies     | String   | 영화 스트리밍 서비스 가입 여부 (Yes/No/No internet service) |
| Contract            | String   | 계약 유형 (Month-to-month/One year/Two year)           |
| PaperlessBilling    | String   | 종이 청구서 여부 (Yes/No)                              |
| PaymentMethod       | String   | 결제 방식 (Electronic check/Mailed check/Bank transfer (automatic)/Credit card (automatic)) |
| MonthlyCharges      | Float    | 월별 요금                                              |
| TotalCharges        | Float    | 총 요금                                                |
| **Churn**           | String   | 이탈 여부 (Yes/No)                                     |

</details>

---

## 1. 문제 정의

통신사 고객 이탈 예측은 기존 고객 데이터를 활용해 어떤 고객이 이탈할 가능성이 높은지 미리 파악하고, 이를 통해 선제적인 마케팅 및 고객 유지 전략을 수립하는 문제입니다.

- **핵심 질문**:  
  - 어떤 고객 특징이 이탈과 연관성이 높은가?  
  - 이탈 가능성이 높은 고객을 어떻게 조기에 식별할 것인가?

---

## 2. 프로젝트 목표

1. **EDA 및 전처리**  
   - 결측치/이상치 처리, 범주형 변수 인코딩, 스케일링 등  
2. **모델링**  
   - 머신러닝(로지스틱 회귀, 랜덤포레스트 등) 및 딥러닝(MLP) 기반 이탈 예측 모델 개발  
3. **모델 성능 평가**  
   - Accuracy, Precision, Recall, F1-score, AUC-ROC 등을 활용한 비교  
4. **시각화 및 인사이트 도출**  
   - 주요 피처 중요도(Feature Importance) 시각화  
   - 이탈 위험 고객 분포 및 추천 액션 플랜 제시  
5. **보고서 및 발표 자료 작성**  
   - 분석 과정, 결과 및 비즈니스 인사이트 정리  

