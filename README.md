# telecom_churn

# 프로젝트 문제 정의 및 목표
# 1️⃣ 프로젝트 일정
| 기간          | 주요 활동                                                                                   |
|--------------|---------------------------------------------------------------------------------------------|
| 5/7     | 프로젝트 기획 (통신사 고객 이탈 예측 모델 생성 및 해당 모델을 통한 개선점 시각화)            |
| 5/8    | EDA, 전처리, 시각화                                                                         |
| 5/9 - 5/10    | 모델링 (머신러닝, 딥러닝 2-way)                                                             |
| 5/11 - 5/14   | 비즈니스 제안서 작성                                                              |


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


# 2️⃣ 프로젝트 기획

1. EDA (Exploratory Data Analysis) 탐색적 데이터 분석
2. 데이터 전처리 수행
    - 불필요 컬럼 삭제
    - 컬럼 내용 변경
    - 컬럼 type 변경
    - 결측치 처리
    - 그룹화
3. 시각화
    - matplotlib, seaborn
    - bar, scatter, countplot, boxplot
4. Modeling
    - AUC-ROC ≥ 0.80, Recall ≥ 0.75 목표
    - 모델별 성능평가 시각화 (Roc Curve 등)
5. 인사이트 도출 및 비즈니스 제안서 작성
    - 예측 결과 기반 맞춤형 유지 전략(예: 요금제 업그레이드, 커뮤니케이션 캠페인) 수립
    - ROI(투자 대비 효과) 시뮬레이션을 통한 우선 순위 제안

# 3️⃣ 프로젝트 정의

### **💡문제 양상 (비즈니스 맥락)**
통신사에서는 고객 확보보다 기존 고객 유지가 더 비용 효율적입니다. 하지만 매월 일정 비율의 고객이 서비스를 해지(Churn)해 매출 손실과 마케팅 비용 증가를 야기합니다.


### **‼️프로젝트 목표**
고객의 인구통계학적 특징, 서비스 이용 패턴, 결제 방식 등을 기반으로 **“다음 달에 어떤 고객이 이탈할 것인가?”**를 예측

### **💼프로젝트 기대효과**
1. 조기 경고: 이탈 가능성이 높은 고객을 사전에 파악하여 맞춤형 프로모션 및 혜택 제공
2. 비용 절감: 불필요한 마케팅 지출 최소화
3. 고객 만족: 개인화된 유지 전략으로 장기 고객 충성도 확보
