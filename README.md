# 1.2 Q-learning 

## 용어 정리

### Q러닝이란?

 Model이 없이 학습하는 강화학습 알고리즘
 
 유한한 마르코프 결정 과정에서 Agent가 특정 상황에서 특정 행동을 하라는 최적의 Policy를 배우는 것
 
 현재 상태로부터 시작하여 모든 연속적인 단계들을 거쳤을 때 전체 보상의 예측갑을 극대화 시킴
 
 "Q"는 현재 상태에서 취한 행동의 보상에 대한 quality를 상징

* Greedy action : Q값이 높은 state로 이동

* Exploration(탐험) : 더 좋은 길을 찾기 위해 수행

* ε - Greedy : ε(0~1) 만큼은 Random하게 나머지는 Greedy하게 수행 

<img src="https://user-images.githubusercontent.com/68425309/201653793-b4267f92-99e9-4be5-b1a8-f2c952fd53cd.jpg" width="300" height="300"/> 

* Exploration & Exploitation (trade off): 새로운 Path , 새로운 맛집!
  - Exploitation(Exploration+ε - Greedy) : Q값을 이용하여 Greedy하게 이동

* (Decaying) ε - Greedy : 탐험을 점점 줄여나간다 (= 입실론을 0.9 -> 0)

* Discount factor(γ) - 0~1사이의 값
  - 조금 더 효율적인 factor를 찾게 해준다
  - 가장 큰 값을 다음 state에서 가져오되, γ를 곱해서 가져온다

* Q-update

<img src="https://user-images.githubusercontent.com/68425309/201660546-b3a688d4-1144-4b91-9925-a483164aefd4.jpg" width="800" height="400"/> 



참조 : <혁펜하임 [강화학습] 1-2강. Q-learning 쉬운 설명 | "맛집 찾기"로 설명하는 강화 학습>
(https://www.youtube.com/watch?v=3Ch14GDY5Y8&list=PL_iJu012NOxehE8fdF9me4TLfbdv3ZW8g&index=2)
