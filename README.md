# 범죄 유형 분류 해커톤

## EDA
### 1.타켓변수의 불균형 확인
![Image](https://github.com/user-attachments/assets/409561ed-e121-4862-9691-fffff3630eb4)

- 타켓변수의 불균형을 확인한 결과 강도의 빈도가 가장 많았다.

### 2. 요일별 타겟분포 확인   
![Image](https://github.com/user-attachments/assets/39a8425c-b722-43e7-b1a3-ae3fa6fd46ce)

- 토요일에 강도 발생 횟수가 가장 많았다.
- 일요일은 상해 빈도수가 많다.
- 주말과 금요일에 범죄 발생 횟수가 급증하는데, 이는 유동인구가 많아서인것으로 추정된다.

### 3. 월별 타겟분포
![Image](https://github.com/user-attachments/assets/4c5d0c9d-49bd-4f1d-a668-86bd2b4e1a67)
- 12월의 데이터 수가 적다.
- 가을에 범죄 발생량이 가장 많고, 겨울에 적은데 이는 12월 데이터의 양이 적어서 그런것으로 추정

### 4. 시간별 분포
   ![Image](https://github.com/user-attachments/assets/d29bd6cb-b19b-4aa4-b319-90eff0365bd3)
- 12시에 범죄가 가장 많이 일어난다.

### 5. 장소에 따른 분포
![Image](https://github.com/user-attachments/assets/5e7e2b83-4ec6-402b-b780-a396fe28fbfa)
- 편의점, 백화점, 약국 등 판매 업소에서 범죄가 많아 일어난다.
- 주차장에서 절도가 많이 일어난다.
- 차도에서 상해가 가장 많이 일어난다.
- 학교, 병원, 공원, 식당, 주유소, 호텔/모텔 등은 특이사항 없음

### 날씨에 따른 분포

![Image](https://github.com/user-attachments/assets/16933781-e077-4a1f-ba65-efcba25a963f)
![Image](https://github.com/user-attachments/assets/154a83e6-7d70-4f38-a43a-7903c6945a0e)

=> 주성분분석 수행

![Image](https://github.com/user-attachments/assets/2e5c2738-f542-4ddc-bb13-8061e3f8d90c)
- 고윳값, 누적 기여율, scree plot을 고려해 주성분의 개수를 5개로 선정 
---
### 모델
XGBOOST
### 평가산식
$\text{F1 Score} = \frac{2}{ \left(\frac{1}{\text{Precision}} + \frac{1}{\text{Recall}} \right) }$
