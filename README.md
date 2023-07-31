<img src="https://www.energydaily.co.kr/news/photo/202211/132051_86204_1454.jpg" width=600 height=400>

# Data Analytics for Incentive
"발전량 예측 정산금" 을 높이기 위한 데이터 분석 프로젝트.

## 개요
산업통상자원부와 한국전력거래소는 [](https://motie.go.kr/motie/gov3.0/gov_openinfo/sajun/bbs/bbsView.do?bbs_seq_n=163324&bbs_cd_n=81) 재생에너지 확대에 따른 출력 변동성 대응을 위해 재생에너지 발전량 예측제도를 도입한다고 밝혔습니다. 

예측제도란 20MW 이상 태양광 및 풍력 발전사업자 등이 재생에너지 발전량을 하루 전에 미리 예측하여 제출하고, 당일 날 일정 오차율 이내로 이를 이행할 경우 정산금을 지급하는 제도입니다.

재생에너지 발전량 예측능력을 제고함으로써 재생에너지 변동성으로 인하여 발전기를 추가 기동𐄁정지하거나 증𐄁감발 하는 비용을 절감하는 등 보다 효율적인 전력계통 운영을 기대합니다.

우리는 최적 예측형 집합자원 모델을 개발함으로써 참여대상인 소규모 전력중개사업자에게 높은 정산금과, 정책품질의 향상을 추구합니다.

## 현재단계
본 분석 과제에서는 2023년 3월 1일부터 3월 31일까지 시간대별로 발전량이 나타나있는 시계열 데이터를 사용하고, 클러스터링 알고리즘을 활용하여 시계열 데이터의 패턴을 식별비슷한 데이터를 그룹으로 묶는 작업을 합니다. 시간대별 오차율 분포를 시각화합니다.

## 향후 진행방향
우리의 목표는 재생에너지 발전량 예측 정산금의 정교한 추정을 위해 clustering 알고리즘 기반 최적 예측형 집합 모델 개발을 목표합니다. 
1. 발전소별 오차율 분석을 위해 고려해야할 요인을 추가
2. 추가된 데이터에서 발전소별 오차율 데이터가 집계되어 있음. 집계데이터에, 통계학 방법/기계학습/딥러닝/그래프 방법론 등을 적용
3. 오차율 데이터를 이용하여 정산금 예측을 위해 다양한 시각적인 그래프, 차트 구현.

## 특징
우리는 예측형 모델 집합 분류에 적합한 방법으로써 머신러닝 기반의 클러스터링 기법을 선정하였다. 훨씬 더 많은 데이터가 있을 경우에는 딥러닝을 사용하는 것이 좋은 선택이지만 학습용 데이터는 총 10,478개(실측데이터 5,239개과 예측데이터 5,239개)로 딥러닝 모델의 학습을 위한 요구 데이터가 충분하지 않다. 따라서, 최적화된 예측형 집합자원을 위한 딥러닝 모델은 과대적합(Overfitting)뿐만 아니라, 일반화 성능이 저하될 수 있다.

## 기술적 요구사항
- 코드 간결화
- 스트링 데이터 수치화
- 오차율 산식 변환  
  - ex) |발전량-예측량| / 설비용량 * 100
- silhoutte 계수를 통한 적합성 판단
- 주석 필수

## 국내 참고자료
- 서울시 빅데이터분석 사례 
- 노인복지시설 현황 분석
- 국내외 논문

## 관련 용어
- 전력계통 : 전력 생산자로부터 전력 소비자에게 전기를 공급하기 위해 상호간에 연결된 네트워크
- Clustering 방법론 : 비지도 학습의 한 종류. 유사한 특성을 가진 데이터 포인트들을 그룹으로 묶는 기법
