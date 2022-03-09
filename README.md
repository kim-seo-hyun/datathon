# datathon

<h3 align="center"> Aiffel YJ2th Datathon Nexflix 1조 ❤weddingpeach❤ </h3>

<div align="center">
  
![웨딩피치_jpg](https://user-images.githubusercontent.com/87296126/157383247-227a90c5-f74a-47ce-af03-0d63541902cb.jpg)
 
</div>

## Discription
- 2022.03.08 ~ 2022.03.11
- Netflix dataset을 바탕으로 한 데이터 분석 및 시각화 프로젝트
- 멤버: 박재경 (팀장)(웨딩피치)/ 김서현(엔젤 릴리)/ 조송희(엔젤 데이지)
- 과정: 데이터 기본 분석> 방향 설정> 데이터 모델링> 데이터 분석> 데이터 시각화> 인사이트 도출 및 마무리

## about datathon
**<평가 방식>** 

- EDA 및 시각화가 적절하게 이루어졌는가? (15%)
- 데이터 분석을 통한 인사이트가 도출이 잘 되었는가? (15%)
- 도출한 인사이트를 통해 설득력이 충분하였는가? (20%)
- 팀원들이 협업을 통해 프로젝트를 수행하고 발표를 진행하였는가? (25%)
- 발표시간을 준수하였는지? (25%)
- 가점 : 교육생들의 따봉 (좋아요 수치를 합산하여 가산점으로 반영)

##  data analysis 

![데이터분석](https://user-images.githubusercontent.com/87296126/157386982-086507e9-5101-4daa-b271-6b8d5ef4d24e.jpg)

### 수집 데이터

- dataset1)Netflix Movies and TV Shows: https://www.kaggle.com/shivamb/netflix-shows?select=netflix_titles.csv
- dataset2)Netflix subscribers and revenue by country: https://www.kaggle.com/pariaagharabi/netflix2020
- dataset3)Netflix Original Films & IMDB Scores: https://www.kaggle.com/luiscorter/netflix-original-films-imdb-scores

### Data organization
1) 내용적 측면: 시간에 따른 자극적인 콘텐츠 변화 추이
  - 비고) main_df.csv 활용
  - 등급, 장르 등으로 확인
2) 구조적 측면: 넷플릭스 오리지널 콘텐츠에 따른 변화 추이
  - 비고) original.csv 활용
  - 넷플릭스 오리지널수의 증감 추이
  - 오리지널과 오리지널이 아닌 콘텐츠의 비교
  - 오리지널과 국가간의 상관관계 등
3) 시장 측면: 국가(대륙) 간 상관관계 분석
  - 비고) cont_df.csv, NetflixsRevenue2018toQ2_2020.csv, NetflixSubscribersbyCountryfrom2018toQ2_2020.csv 활용
  - 수익, 구독자 수와의 상관관계 분석

### Data Modeling Relationship
![dataset_relationship](https://user-images.githubusercontent.com/87296126/157394791-27f7fc01-9b73-4240-977f-901113fa46e0.jpg)

### 분석 목표에 따른 분석 기법

| 분석목표 | 설명 | 통계적 분석 기법 | ✔
|---|:---:|:---:|:---:|
평균에 대한 검정과 추정 | 평균값에 대한 모델링 | T검정
비율에 대한 검정과 추정 | 비율에 대한 모델링 | 직접확률계산법, F분포법
분할표의 검정 | 각각 2개 이상의 분류값을 지닌 2개 이상의 차원이 있고 그 결과로 하나의 측정값이 있을 때, 분류 조합에 따라 측정값에 유효한 차이가 발생하는지를 검정 | 카이제곱 검정, Fisher의 직접 확률 검정, 맥네마의 검정, 잔차 분석
변수들 간의 상관관계의 강도 도출 | 독립적으로 움직이는 두 변수들 사이의 관계(상관관계)의 강도를 상관계수로 나타내어 표시 | 상관분석 | ✔
변수들 간의 선형/ 비선형 인과관계의 형태와 강도 추출 |종속적으로 움직이는 두 개 이상의 변수들 사이의 관계의 강도를 결정 계수로 나타내고, 각 변수의 계수를 추정해 모델화, 변수들은 연속적인 값일 수도 있고 분류값일 수도 있음 | 회귀분석, 다중회귀분석, 로지스틱 회귀분석, 판별분석 | ✔
어떤 결과에 영향을 미치는 요인들 사이의 관계와 핵심 요인의 선별 |어떤 측정값에 변화 요인이 되는 값들이 세 개의 차원이 라고 할 때, 각 차원들 중에 어떤 것이 측정값에 가장 큰 영향을 미치는지, 각 차원은 다른 차원의 영향력과 어느 정도 겹치는지 분석 | 요인분석, 주성분분석
대상들을 여러 기준값들에 따라 분류하고, 다차원 공간에 배치 | 측정값과 차원들이 있을 때 차원들의 값을 기준으로 측정값들 사이의 거리를 계산해 적절하게 그룹을 짓고, 이 거리가 의미있는 차원들로 축을 구성한 다차원 공간에 측정값들을 배치 | 군집분석, 다차원척도법(MDS) | ✔
차원들의 패턴이 비슷한 측정값과 그렇지 않은 측정값을 분류 | 예를들어, 설문 항복에 대한 답변들의 패턴에 따라 비슷한 답변을 한 응답자와 그렇지 않은 응답자를 분류 | 대응분석
시간의 흐름에 따라 변하는 데이터를 분석할 수 있는 모델의 도출 | 시계열 데이터에 영향을 주는 요인을 추세요인, 계절요인, 순환요인, 불규칙요인으로 분해해서 시계열 데이터를 가장 잘 설명할 수 있는 모델을 만들고, 이 모델을 통해 미래에 대해서도 예측 | 시계열 분석 | ✔

### Data visualization

- toolbox: matplotlib, seaborn, plotly, volia
- 시간 시각화 : 막대그래프, 누적 막대 그래프, 점 그래프
- 분포 시각화 : 원그래프(파이차트), 도넛차트, 트리맵, 누적 연속 그래프분포
- 관계 시각화 : 스캐터 플롯(산점도), 버블 차트, 히스토그램
- 비교 시각화 : 히트맵, 체르노프 페이스, 스타차트, 평행좌표계, 다차원척도법
- 공간 시각화 : 지도 매핑

## Finish

참고)
- process: https://brunch.co.kr/@data/10
- 시각화: https://mizykk.tistory.com/61
