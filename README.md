# 프로젝트 문제 정의 및 목표
<p align="center">
  <img src="https://github.com/user-attachments/assets/5712810a-0a79-4a96-b994-3fdbe5019ef2" width=600>
</p>

## 1. 프로젝트 일정
| 기간          | 주요 활동                                                                                   |
|--------------|---------------------------------------------------------------------------------------------|
| 5/7     | 프로젝트 기획            |
| 5/8    | EDA, 전처리, 시각화                                                                         |
| 5/9 - 5/10    | 모델링                                                             |
| 5/11 - 5/14   | 비즈니스 제안서 작성                                                              |

## 2. 팀원

<table>
  <tbody>
    <tr>
      <td align="center">
        <a href="https://github.com/PARKYUNSU">
          <img src="https://avatars.githubusercontent.com/PARKYUNSU?size=100" width="100px;" alt="PARKYUNSU"/>
          <br /><sub><b>PARKYUNSU</b></sub>
        </a>
      </td>
      <td align="center">
        <a href="https://github.com/LoveBird-cute">
          <img src="https://avatars.githubusercontent.com/LoveBird-cute?size=100" width="100px;" alt="LoveBird-cute"/>
          <br /><sub><b>LoveBird-cute</b></sub>
        </a>
      </td>
      <td align="center">
        <a href="https://github.com/jinijiniin">
          <img src="https://avatars.githubusercontent.com/jinijiniin?size=100" width="100px;" alt="jinijiniin"/>
          <br /><sub><b>jinijiniin</b></sub>
        </a>
      </td>
      <td align="center">
        <a href="https://github.com/Dong-Kyu-Lee7">
          <img src="https://avatars.githubusercontent.com/Dong-Kyu-Lee7?size=100" width="100px;" alt="Dong-Kyu-Lee7"/>
          <br /><sub><b>Dong-Kyu-Lee7</b></sub>
        </a>
      </td>
      <td align="center">
        <a href="https://github.com/bluol">
          <img src="https://avatars.githubusercontent.com/bluol?size=100" width="100px;" alt="bluol"/>
          <br /><sub><b>bluol</b></sub>
        </a>
      </td>
    </tr>
  </tbody>
</table>


## 3. 프로젝트 기획

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

## 4. 프로젝트 정의

### **💡문제 양상 (비즈니스 맥락)**
   통신사에서는 고객 확보보다 기존 고객 유지가 더 비용 효율적입니다. 하지만 매월 일정 비율의 고객이 서비스를 해지(Churn)해 매출 손실과 마케팅 비용 증가를 야기합니다.


### **‼️프로젝트 목표**
   고객의 인구통계학적 특징, 서비스 이용 패턴, 결제 방식 등을 기반으로 **“다음 달에 어떤 고객이 이탈할 것인가?”**를 예측

### **💼프로젝트 기대효과**
1. 조기 경고: 이탈 가능성이 높은 고객을 사전에 파악하여 맞춤형 프로모션 및 혜택 제공
2. 비용 절감: 불필요한 마케팅 지출 최소화
3. 고객 만족: 개인화된 유지 전략으로 장기 고객 충성도 확보

## 5. EDA
