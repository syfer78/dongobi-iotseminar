사물인터넷을 위한 머신러닝/딥러닝
=============

## 스키너의 쥐 실험
![Skinner](http://image.yes24.com/blogimage/blog/h/w/hws321/9iaoJ0BP.jpg)

## 확률계(Stochastic System)에서의 순차적 의사 결정(Sequential Decision) 문제

![Agent Environment Interface](https://blog.kakaocdn.net/dn/uiaEg/btqyMrckJ6K/bAlYp8C6hhFQJadmozh5ok/img.png)

* Stochastic System : For a system to be stochastic, one or more parts of the system has randomness associated with it.
* Sequential Decision Making : Agent와 World가 서로에게 영향을 주면서 연속적인 결정을 만들어 나가는 것 여기에서 최종 목적은 Agent가 받을 기대보상의 최대화.
Agent는 항상 당장의 보상과 미래에 받을 수 있는 보상 두 가지를 고려해서 결정해야 함.
* Markov Decision Process : 마르코프 결정 과정은 이산 시간 확률 제어 과정(discrete time stochastic control process)이다. 어떤 시점에, 마르코프 결정 과정은 어떤 상태 {\displaystyle s}s에 존재한다. 의사결정자는 해당 상태 {\displaystyle s}s에서 어떤 행동 {\displaystyle a}a를 취할 수 있으며, 다음 시점에서 마르코프 결정 과정은 확률적으로 새로운 상태 {\displaystyle s'}{\displaystyle s'}로 전이한다. 이 때 의사결정자는 상태 전이에 해당하는 보상 {\displaystyle R_{a}(s,s')}{\displaystyle R_{a}(s,s')}을 받는다. 기존의 상태 {\displaystyle s}s에서 새로운 상태 {\displaystyle s'}{\displaystyle s'}로 전이하는 확률은 의사결정자의 행동에 영향을 받는다. 즉, 전이 확률 함수는 {\displaystyle P_{a}(s,s')}{\displaystyle P_{a}(s,s')}와 같이 주어진다. 따라서, 다음 상태 {\displaystyle s'}{\displaystyle s'}는 현재 상태 {\displaystyle s}s와 의사결정자의 행동 {\displaystyle a}a에만 영향을 받으며 이전의 모든 상태와는 확률적으로 독립적이므로, 마르코프 결정 과정의 상태 전이는 마르코프 속성을 만족한다.

## 강화학습(Reinforcement Learning)이란?
* 현재의 상태(State)에서 최적의 행동(Action)을 선택하는 방법을 학습
>어떤 환경(Environment)안에서 행동의 주체인 에이전트(Agent)가 선택 가능한 행동(Action)들 중 보상(Reward)을 최대화하는 행동 또는 행동 순서를 선택하도록 학습하는 방법

* State : 머신 러닝을 통하여 해결하려는 문제
* Action : 머신 러닝의 입력값. 즉 학습 데이터를 의미.
* Reward : 머신 러닝의 결과. 즉 예측치, 분류값 등의 목적한 결과값.
* Policy : 머신 러닝의 결과. 즉 예측치, 분류값 등의 목적한 결과값.
* Value function : 머신 러닝의 결과. 즉 예측치, 분류값 등의 목적한 결과값.

## 심층 강화 학습 (Deep Reinforcement Learning)
### 1.가치 기반 방법
* 알고리즘이 가치 함수를 최대화 하는 행동을 취함. 목표는 최적 가치를 찾는데 있음.
  
### 2.정책 기반 방법
* 가치 함수를 최대화 하는 최상의 정책을 예측. 목표는 최적의 정책을 찾는 것.

## OpenAI Gym
* Agent 훈련을 위한 환경 모음

## Greedy Algorithm(그리디 알고리즘)
* 미래를 생각하지 않고 각 단계에서 가장 최선의 선택을 하는 기법 : Q(s,a)=r(s,a)
* 탐험(Exploration)이 충분히 이루어지지 않았기 때문 최선의 결과가 나올지 알 수 없음

## E-Greedy Algorithm(입실론 그리디 알고리즘)
* 그리디 알고리즘에서 일정 확률로 랜덤한 행동을 취하도록 하는 알고리즘
* 0 < ϵ < 1 인 어떤 ϵ 값을 이용해서, 탐험과 활용을 적절히 번갈아가며 사용

## The Bellman Equation
* 벨만 방정식 : Q(s,a)=r(s,a)+γmaxQ(s′,a)
                             a
* 모든 보상의 총합은 현재 행동을 취해서 받을 수 있는 즉각보상과 미래에 받을 미래보상의 최대값의 합
* Agent의 목표 : 총합을 최대화 할 수 있는 행동을 선택해내는 것
* Markov States 가정이 유효하다면, 벨만 방정식의 재귀적인 성질은 미래에 받을 수 있는 보상을 멀리 떨어진 과거로까지 전파
* 벨만 방정식의 재귀적인 성질은 또한, 처음에 실제 Q값이 얼마인지 알지 못해도 추측으로 값을 정해서, 정답으로 수렴

## Q-Learning
* 최적의 행동 선택 정책을 배우기 위한 알고리즘

Q Table 초기화 -> Action 선택 -> Action 수행 -> 보상 측적 -> Q Table 갱신 -> Action 선택

## Q-Network 
Q-Learning에는 상태 공간과 행동 공간의 제약이 존재하므로
Q-table 대신 신경망을 사용해서, 그 신경망 모델이 Q 가치를 근사해낼 수 있도록 학습


## 관련 영상
https://www.youtube.com/watch?v=w1MF0Iz0p40&t=44s
https://www.youtube.com/watch?v=_KL5iU_nXEs
https://youtu.be/goxCjGPQH7U