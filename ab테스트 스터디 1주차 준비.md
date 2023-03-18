# 윤훈영

주차: 1주차

### 통계 공부

---

- 통계수업 다음을 참고하세요
    
    Descriptive Statistics(기술 통계) [https://www.udacity.com/course/intro-to-descriptive-statistics--ud827](https://www.udacity.com/course/intro-to-descriptive-statistics--ud827) 
    
    Inferential Statistics(추론 통계) [https://www.udacity.com/course/intro-to-inferential-statistics--ud201](https://www.udacity.com/course/intro-to-inferential-statistics--ud201)
    

### 1. A/B 테스트란

---

- 온라인에서 어떤 기능(feature)이나 제품(product)이 더 나은 버전인지를 확인하기 위해 진행하는 일반적인 방법론
- Gerylock의 John은 ‘A/B테스트는 산의 정상에 도달하는데 효과적이지만, 이 쪽 산과 저 쪽 산의 정상이 나은지를 판단하는데는 유용하지 않다’라고 말했다 → A/B테스트는 **제품 개발 프로세스의 일부**라는 것
- 온라인 실험은 사용자에 대한 해상도는 낮지만, 모수가 많음 → 따라서 사용자를 정확하게 식별하는게 중요
- 실험의 궁극적인 목적은 “더 좋은 제품을 만들어나가는데 인사이트를 찾고 이를 반복하기 위함”

![Untitled](%E1%84%8B%E1%85%B2%E1%86%AB%E1%84%92%E1%85%AE%E1%86%AB%E1%84%8B%E1%85%A7%E1%86%BC%2022e6dbc812e644f8a4402a20af5d0e60/Untitled.png)

출처 : [https://gohighbrow.com/the-summit-app-ab-testing/](https://gohighbrow.com/the-summit-app-ab-testing/)

- 새로운 경험과 장기적인 비즈니스 지표를 측정하는데는 실험은 효과적이지 않을 수 있다.
    - 비교를 위한 베이스라인이 무엇인가? (이 새로운 경험이 낫다는 것을 판단할 수 있는 기준이 이써???)
    - 의사결정을 하기까지 얼마나 시간이 걸릴까? → Plateau에 도달하기까지 (Primary Effect, Novelty Effect를 고려하면 어떤데에ㅔ???)
- 유명한 A/B 테스트 예시들
    
    한글 아티클 추천 : [넷플릭스가 영상에 적합한 삽화를 찾은 방법](https://www.mobiinside.co.kr/2020/10/05/hackle/)
    
    **Examples mentioned in the video:**
    • Google **[tested 41 different shades of blue](http://www.nytimes.com/2009/03/01/business/01marissa.html?pagewanted=3)**.
    • Amazon initially decided to launch their first personalized product recommendations based on an **[A/B test showing a huge revenue increase by adding that feature](http://www.exp-platform.com/Documents/GuideControlledExperiments.pdf)**. (See the second paragraph in the introduction.)
    • LinkedIn **[tested whether to use the top slot on a user's stream for top news articles or an encouragement to add more contacts](http://engineering.linkedin.com/mobile/mobile-ab-testing-linkedin-how-members-shape-our-apps)**. (See the first paragraph in "A/B testing with view based JSON" section.)
    • Amazon determined that **[every 100ms increase in page load time decreased sales by 1%](http://www.exp-platform.com/Documents/IEEEComputer2007OnlineExperiments.pdf)**. (In "Secondary metrics" section on the last page)
    • Google’s **[latency results](http://googleresearch.blogspot.com/2009/06/speed-matters.html)** showed a similar impact for a 100ms delay.
    **Other Examples:**
    • Kayak **[tested whether notifying users that their payment was encrypted would make users more or less likely to complete the payment](http://apptimize.com/blog/2014/03/kayaks-most-interesting-ab-test/)**.
    • Khan Academy tests **[changes like letting students know how many other students are working on the exercise with them, or making it easier for students to fast-forward past skills they already have](http://apptimize.com/blog/2014/07/how-khan-academy-uses-ab-testing-to-improve-student-learning/)**. (See the question "What is the most interesting A/B test you've seen so far?")**이전다음페이지 피드백 보내기**
    

### 2. A/B 테스트로 할 수 있는 것과 없는 것

---

- 다양한 예시
    - **추천 알고리즘 → 실험을 하기에 가장 적합하다**
    - **초기 페이지의 레이아웃 (UI변경) → 매우 적합**
    - 커머스 사이트 완성여부 판단 → 특정 상품에 대한 것은 실험해볼 수 있으나, 일반적인 경향성에 대해서 설명하긴 어렵다
    - 프리미엄 서비스 제공 → 정보를 얻을 순 있겠지만, 완전히 테스트하기 어렵다
    - 백엔드 인프라 변경 → 컴퓨팅 파워가 충분하면, 해볼 수 있다
    - 레퍼럴 프로그램 → 리드타임이 길어서 실험하기 적합하지 않다
    - 뉴 브랜딩 → 데이터에 기반해서 결정하기에 감정적인 영역
- 설계적인 차원
    - 실험군과 대조군간 발생하는 파급효과(Spillover Effect)가 발생할 수 있을 때
- 상황 차원
    - 내부 리소스 : A/B 테스트를 지원할 수 있는 인프라가 갖춰지지 않았을 때
    - 다른 검증 방식 : 다른 검증 방식을 통해 니즈에 대한 확신이 강할 때
    - 유저 경험에 악영향 : 유저 경험을 크게 해칠 위험이 있을 때
    - 매출에 악영향 : 매출에 큰 타격을 입힐 수 있을 때, 테스트의 비용이 높아진다
    - early stage : 실험을 진행하기에 충분한 트레픽을 확보하기 어려울 때

### 3. A/B 테스트 외에 활용가능한 기술

---

- 고객행동데이터에 기반해서 데이터 분석을 해라!
- 데이터에 기반한 인사이트의 종류

| 유형 | 설명 | 예시 |
| --- | --- | --- |
| Observational | 현상, 환경, 행동을 설명하는 것을 기반으로 하는 인사이트 | 유저들이 홈페이지에서 오래 체류 → 홈페이지를 더 탐색하기 좋고 정리된 형태로 개선하자 |
| Comparative | 두가지 서로 다른 수량간의 비교를 통한 인사이트 | 오거닉 유저의 유입이 저번달 대비 크게 감소 → 감소 원인을 찾자 |
| Causal | 다른 요소를 발생시키는 하나의 요소에 대한 인사이트 | 프로모션을 조회하는 것은 유저로 하여금 핸드백을 구매하게 한다 → 프로모션을 더 많이 유저가 조회하게 하면 더 많은 핸드백 구매로 이어질 것이다 |
| Predictive | 미래에 발생할 요소에 대한 인사이트 | 앞으로 인구가 비슷한 비율로 증가하면, 20년에는 5배 더 큰 warehouse필요할 것 → 더 큰 warehouse를 구축할 계획을 세우자 |
- 인과 관계를 밝히는 여러 방법론

| Randomization | A/B 테스트 |  |
| --- | --- | --- |
|  | MAB(Multi-Armed Bandits) | A/B테스트에 사용되는 최적화 알고리즘. MAB에서 테스트 중인 다양한 슬롯 머신은 ‘팔’에 비유됨. 시간이 지남에 따라 어떤 버전이 잘 수행되는지 학습하고, 팔의 우선순위를 지정해서 최상의 옵션이 제공되도록 함. → 마케팅(광고)에서 가장 많이 사용됨 |
| Naturual Experiment | Regression Discontinuity(회귀 불연속성) | 사회과학, 경제연구에서 인과 효과를 평가하는데 사용하는 통계적 방법.  |
|  | Instrumental Variable(IV) | A/B테스트의 실험군, 대조군 할당 여부를 도구 변수를 활용해서 알고자하는 인과 관계를 추정하는 방식 |
|  | Lookforward Matching |  |
|  | Difference In Differences | 시간 경과에 따른 실험군, 대조군 간의 결과 변화를 비교하여 인과 효과를 추정하는 방법 |
| Conditioning | Stratification | 모집단을 계층으로 그룹화해서 교란 변수를 제어하는데 사용되는 방식 |
|  | Matching Propensity Scores(성향 점수 매칭) | 연구 대상의 balance를 맞추기 위해 매칭을 통해 imbalance한 효과를 피한다. Logistic Regression을 통해서 처치군(1), 대조군(0)으로 하는 이항반응 형태로 종속변수를 설정하고 보정하려는 공변량을 독립 변수로 지정하고 회귀분석 시행. 이 모형에 의해 각 대상들이 추정된 확률이 propensity score에 해당함 |

### 4. 지표

---

ex. 가상의 온라인 금융교육을 제공하는 서비스 <Audacity>

![Untitled](%E1%84%8B%E1%85%B2%E1%86%AB%E1%84%92%E1%85%AE%E1%86%AB%E1%84%8B%E1%85%A7%E1%86%BC%2022e6dbc812e644f8a4402a20af5d0e60/Untitled%201.png)

- Customer Funnel : 홈페이지 방문 -> 탐색 -> 계정 생성 -> 완료
- 실험 가설 : “시작하기”버튼을 주황 -> 핑크로 변경하면 더 많은 학생들이 Audacity 코스를 탐색할 것이다
- 목표 지표(OEC) : 고유 클릭 수 / 고유 페이지 뷰 수 (전환율을 중심으로 보는 것이 좋다)
- 사용하지 않는 지표
    - 클릭 수 / 페이지 뷰 수 (CTR)
    - 완료된 코스의 숫자 (너무 많은 시간이 사용되어 실용적이지 않음)
    - 클릭 수

### 5. 이항 분포

---

- 결과가 2가지 있을 때 (성공, 실패)
- 독립적인 이벤트
- 독립적인 분배

섞인 카드들 중에서 고르기 (빨강vs블랙) - 뽑은 카드가 다음 카드에 영향을 줌으로 독립적인 이벤트가 아님

주사위 던지기 - 독립시행임

### 6. 통계적 검증

---

- 신뢰 구간
- 통계적 유의성

**+) 번외 실험을 진행하는 데이터분석가에게 중요한 과제와 필요 역량**

1. 실험을 설계하는 과정에서 올바른 지표를 목표로 정하는 것 : 데이터 관리+도메인 지식+통계지식
2. 정해진 시간 내에 신뢰도 높은 결과를 도출하고 의사결정권자가 이해할 수 있도록 돕는 것 : 검증과 커뮤니케이션 역량

### 더 알아보기

---

- [프로덕트 애널리틱스에서 인과추론 활용 사례](https://www.youtube.com/watch?v=ubuFDpYIqTM&t=1275s)
- [https://velog.io/@otzslayer/AB-테스트-톺아보기](https://velog.io/@otzslayer/AB-%ED%85%8C%EC%8A%A4%ED%8A%B8-%ED%86%BA%EC%95%84%EB%B3%B4%EA%B8%B0)
- [실무자를 위한 인과추론 활용 : Best Practices](https://www.slideshare.net/choibokyung/pap-best-practices)
- [https://brunch.co.kr/@539insight/139](https://brunch.co.kr/@539insight/139)