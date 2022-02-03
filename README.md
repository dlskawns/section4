# 리뷰기반 고객 집단 분류 및 딥러닝 기반 추천 알고리즘 
  
이커머스 데이터의 리뷰 분석을 통해 상품평 관련 키워드를 추출합니다.
고객 세분화를 진행하여 해당 정보를 바탕으로 추천시스템 모델링을 목표합니다.

<br>

### 프로젝트 주제 선정 이유:

* 디지털 산업 수요증가 - 이커머스, OTT플랫폼, SNS마케팅 등

* 디지털 산업 경쟁 심화 - 지그재그인수(카카오), 배민라이브쇼핑, 디즈니플로스, 애플TV+ 등 

* 고객 유지, 이탈률 최소화

* 차별적 시스템, 서비스 도입 필요

* 개인적인 디지털 산업에 대한 커리어 목표 및 관심

<br>

### 데이터 셋 Features 설명

출처: Kaggle  

데이터셋 명/파일명/용량: Amazon Fine Food Reviews / Review.csv / 300.9 mb  

#### Columns

Id(int): 샘플별 고유값  
ProductId(str): 상품Id로 해싱처리 되어있음  
UserId(str): 고객Id로 이역시 해싱처리 되어있음  
ProfileName(str): 고객이 설정한 계정 이름  
HelpfulnessNumerator(int): 해당 리뷰가 도움이 된다고 추천한 고객 수  
HelpfulnessDenominator(int): 추천을 동의하거나 하지 않은   
Score(int): 리뷰를 쓴 고객이 해당 상품에 매긴 평점  
Time(timestamp): 리뷰가 작성된 날짜 데이터. 타임스탬프 형식  
Summary(str): 고객 리뷰 데이터의 제목  
Text(str): 고객 리뷰 데이터 전문  

<br>

### 프로젝트 데이터 셋 & 선정 이유:

* 고객 행동 기반 데이터를 통해 자사(플랫폼 및 쇼핑몰 운영사) 고객의 이탈 원인 파악이 필요  
* 날짜 데이터(timestamp)를 통해 언제 구매가 줄었는지 파악  
* 평점(Score)를 통해 해당 고객들의 이탈과 점수의 상관관계 파악  
* 리뷰(Text)를 분석해 고객의 니즈와 불만을 파악 가능  

<br>

<br>

### 분석 및 모델링 진행 방법

* EDA를 통해 각 Feature간 관계 파악. 인사이트 도출  
* Review Text를 분석해 키워드 추출, Top 키워드로 데이터 도메인관련 전반 내용 습득  
* 키워드 또는 인사이트를 반영해 필요 Feature 생성  
* 해당 DCN(Deep & Cross Network)모델을 통해 각 Feature를 임베딩하여 Score를 예측하도록 학습  
* 유저 선정 시, 높은 Score를 가지는 제품 TOP 10 추천진행  









