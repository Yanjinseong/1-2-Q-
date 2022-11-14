# 1.2 Q-learning 

## 용어 정리
* Greedy action : Q값이 높은 state로 이동

* Exploration(탐험) : 더 좋은 길을 찾기 위해 수행

* ε - Greedy : ε(0~1) 만큼은 Random하게 나머지는 Greedy하게 수행 

<img src="https://user-images.githubusercontent.com/68425309/201653793-b4267f92-99e9-4be5-b1a8-f2c952fd53cd.jpg" width="300" height="300"/> 

* Exploration & Exploitation (trade off): 새로운 Path , 새로운 맛집!
  - Exploitation : Q값을 이용하여 Greedy하게 이동

* (Decaying) ε - Greedy : 탐험을 점점 줄여나간다 (= 입실론을 0.9 -> 0)

* Discount factor(γ) - 0~1사이의 값
  - 조금 더 효율적인 factor를 찾게 해준다
  - 가장 큰 값을 다음 state에서 가져오되, γ를 곱해서 가져온다
