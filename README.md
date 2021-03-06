# <div align="center">Paddle-Paddle-NLP-Model_based_Classification-of-Chinese-News-Categories_Project </div>

## 1. 프로젝트 주제
Paddle-Paddle 딥러닝 프레임워크 기반 Robert 사전 학습모델(Pre-trained Model)을 적용한 중국 신문 주제(카테고리) 분류 프로젝트 

<P>

<div align="center"><IMG src='https://user-images.githubusercontent.com/78430460/146801028-b26eec72-c1c3-4e3e-beba-44ef8d60f3b9.png' height=30% width=30%></div> <P>

- Paddle-Paddle?

  패들패들(飞桨)이란 중국 바이두(百度)에서 개발한 딥러닝 프레임워크이다.
  <br>
  (공식 사이트 : http://www.paddlepaddle.org)
<br>
<P>

<div align="center"><IMG src='https://user-images.githubusercontent.com/78430460/146803095-f3548a6f-032a-4c47-a005-843c1e710faf.png' height=60% width=60%></div> </P>


- Robert 사전 학습모델?
  
  Paddle-NLP에서 제공하는 사전 학습 언어 모델로서, Tokenizer와 타겟 변수 클래스 분류를 위한 SequenceClassification 기능을 수행한다.   

## 2. 프로젝트 개요

Paddle-NLP에서 제공하고 있는 Robert 사전 학습모델을 사용하여(사전 학습모델을 사용하므로써, 모델링 간 모델의 성능을 향상시킬 수 있다) 14개의 클래스로 구성된 타겟 변수(신문 주제 카테고리)에 대해 주어진 기사글(특성 변수)-타겟 변수 간 다중 분류값을 분류하기 위한 모델을 학습시키고 실제 테스트 데이터에 적용하므로서 예측할 수 있다.  
  
## 3. 프로젝트 목적

중국어 자연어에 대한 이해력을 바탕으로, 언어 모델에 대한 심화된 이해력을 갖추고 다양한 딥러닝 프레임워크를 사용하고, 사전 학습모델에 대해 이해할 수 있으며 더 나아가 딥러닝 기술 활용 역량 강화를 목표로 한다.
  
## 4. 프로젝트 문제 정의

- 프로젝트 가설 : 주어진 데이터의 특성 변수를 통해 신문 기사 카테고리(타겟 변수)의 다중 분류 값을 예측할 수 있다.

- 프로젝트 예상 결과 : 딥러닝 모델링을 통해 다중 분류의 값을 학습시키고 정확도를 측정한다.
  
## 5. 프로젝트 데이터 

<P>
  
<div align="center"><IMG src='https://user-images.githubusercontent.com/78430460/146805836-5d752e88-b7c9-4baf-b7ec-0fee8031cd3e.png' height=50% width=50%></div> </P>

중국 SNS 플랫폼인 新浪微博(시나 웨이보) 출처 데이터로서, "과학기술, 체육, 엔터테인먼트, 정치, 사회, 교육 등 14개의 카테고리의 주제 기사가 포함된 약 83만개(학습/검증), 84,000개(테스트)의 데이터로 구성되어 있다. 주제 다중 분류를 수행하는 본 프로젝트에 데이터로 사용하기에 적절하다고 판단해 해당 데이터를 사용하여 프로젝트를 수행했다.

### 데이터 미리보기

<div align="center"><IMG src='https://user-images.githubusercontent.com/78430460/146806493-718b566f-eaa3-4f76-be4a-16bdccc130af.png' height=40% width=40%></div> </P>

- 데이터 설명 : 학습/검증/테스트로 구성된 데이터로서, 학습-검증 데이터는 기사글과 대응하는 신문 주제 카테고리로 구성되어 있으며, 테스트 데이터는 라벨값이 포함되어 있지 않다. 

## 6. 프로젝트 분석 방법 

### 데이터 전처리 도식화  
<div align="center"><IMG src='https://user-images.githubusercontent.com/78430460/146808785-528e872f-8454-48b6-a008-615d9491afd8.png' height=60% width=60%></div> </P>

- trans_func 함수를 통한 Raw 데이터에 Robert Tokenizer 적용 및 문서 데이터 벡터화(수치화)
- batchify_fn 함수를 통한 모델링에 사용될 데이터에 대한 배치 사이즈 구성 및 적용
  
분석 방법 : 프로젝트 데이터를 모델링 적용을 위해 Robert 사전 학습모델을 통해 토크나이징, SequenceClassification 등의 전처리 과정을 거친 후, 사전 학습 모델을 적용한 모델링을 통해 데이터를 학습시키고 모델 성능 지표로서 모델 정확도와 로스값을 사용하여 결과 분석을 하고 학습된 모델을 실제 테스트 데이터에 적용하므로써, 다중 분류값(신문 주제 카테고리)을 테스트 데이터에 매칭시켜 결과값을 확인하고 평가한다. 
  
## 7. 프로젝트 결과 분석

학습 데이터를 통한 모델링 및 검증 데이터를 통한 모델 평과 결과 검증 데이터에 대한 모델 정확도는 0.96206, 로스값은 0.11553로 비교적 높게 나왔으며 이를 테스트 데이터에 다중 분류값을 매칭시켜 분류값이 정확하게 구성되었는지 평가했다. 아래의 그림은 테스트 데이터에 타겟 변수값을 매칭시킨 상위 20개의 실제 데이터 값이다.  

<P>  
<div align="center"><IMG src='https://user-images.githubusercontent.com/78430460/146808397-f4778b41-81ce-4022-afd3-c75ebd18b4ef.png' height=30% width=30%></div> </P>
