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

<div align="center"><IMG src='https://user-images.githubusercontent.com/78430460/146803095-f3548a6f-032a-4c47-a005-843c1e710faf.png' height=60% width=60%></div> <P>


- Robert 사전 학습모델?
  
  Paddle-NLP에서 제공하는 사전 학습 언어 모델로서, Tokenizer와 타겟 변수 클래스 분류를 위한 SequenceClassification 기능을 수행한다.   

 
## 2. 프로젝트 개요

Paddle-NLP에서 제공하고 있는 Robert 사전 학습모델을 사용하여(사전 학습모델을 사용하므로써, 모델링 간 모델의 성능을 향상시킬 수 있다) 14개의 클래스로 구성된 타겟 변수(신문 주제 카테고리)에 대해 주어진 기사글(특성 변수)-타겟 변수 간 다중 분류값을 모델 학습시키고 실제 테스트 데이터를 통해 예측할 수 있다.  
  

  
  
 
