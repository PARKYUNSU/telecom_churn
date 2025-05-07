# telecom_churn
팀 프로젝트-통신사 고객 이탈 예측 프로젝트


# 1️⃣ 프로젝트 일정

5.7 ~ : 프로젝트 기획 (통신사 고객 이탈 예측 모델 생성 및 해당 모델을 통한 개선점 등 시각화)

5.8 ~ : EDA, 전처리, 시각화

5.9 ~ : 모델링 (머신러닝, 딥러닝 2way)

~ 5.14 : 프로젝트 내용 및 성과 정리

**Dataset :** https://www.kaggle.com/code/makeyman/telcom-eda

- **Datacard**
    
    ## Data Card: Telco Customer Churn
    
    | **Attribute** | **Details** |
    | --- | --- |
    | **Dataset Name** | Telco Customer Churn |
    | **Source** | Kaggle |
    | **Instances** | 7,043 customers |
    | **Features** | 21 columns (20 features + 1 target) |
    | **Target** | Churn (Yes/No) |
    
    ### Feature Description
    
    | Feature | Type | Description |
    | --- | --- | --- |
    | customerID | string | Unique customer identifier. |
    | gender | categorical | Customer gender (Male, Female). |
    | SeniorCitizen | binary | Indicates if the customer is a senior citizen (1 = Yes, 0 = No). |
    | Partner | binary | Whether the customer has a partner (Yes, No). |
    | Dependents | binary | Whether the customer has dependents (Yes, No). |
    | tenure | integer | Number of months the customer has stayed with the company. |
    | PhoneService | binary | Whether the customer has a phone service (Yes, No). |
    | MultipleLines | categorical | Whether the customer has multiple phone lines (Yes, No, No phone service). |
    | InternetService | categorical | Customer’s internet service provider (DSL, Fiber optic, No). |
    | OnlineSecurity | categorical | Whether the customer has online security service (Yes, No, No internet service). |
    | OnlineBackup | categorical | Whether the customer has online backup service (Yes, No, No internet service). |
    | DeviceProtection | categorical | Whether the customer has device protection service (Yes, No, No internet service). |
    | TechSupport | categorical | Whether the customer has tech support service (Yes, No, No internet service). |
    | StreamingTV | categorical | Whether the customer has streaming TV service (Yes, No, No internet service). |
    | StreamingMovies | categorical | Whether the customer has streaming movies service (Yes, No, No internet service). |
    | Contract | categorical | Contract term of the customer (Month-to-month, One year, Two year). |
    | PaperlessBilling | binary | Whether the customer has paperless billing (Yes, No). |
    | PaymentMethod | categorical | Payment method (Electronic check, Mailed check, Bank transfer (automatic), Credit card (automatic)). |
    | MonthlyCharges | float | The amount charged to the customer monthly. |
    | TotalCharges | float | The total amount charged to the customer. |
    | Churn | binary | Whether the customer churned (Yes, No). |

---

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

<aside>
💡

### **문제 양상 (비즈니스 맥락)**

통신사에서는 고객 확보보다 기존 고객 유지가 더 비용 효율적입니다. 하지만 매월 일정 비율의 고객이 서비스를 해지(Churn)해 매출 손실과 마케팅 비용 증가를 야기합니다.

</aside>

<aside>
❕

### **프로젝트 목표**

고객의 인구통계학적 특징, 서비스 이용 패턴, 결제 방식 등을 기반으로 “다음 달에 어떤 고객이 이탈할 것인가?”를 예측

</aside>

<aside>
💼

### **프로젝트 기대효과**

1. 조기 경고: 이탈 가능성이 높은 고객을 사전에 파악하여 맞춤형 프로모션 및 혜택 제공
2. 비용 절감: 불필요한 마케팅 지출 최소화
3. 고객 만족: 개인화된 유지 전략으로 장기 고객 충성도 확보
</aside>
