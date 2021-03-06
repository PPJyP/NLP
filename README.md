<div align="center">
  
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=200&section=header&text=NLP&fontSize=50" />
  
</div>

- 아래는 구현할 **NLP관련 알고리즘**을 설명
- [알고리즘명] 아래 해당되는 **파일명** 기재

<br/><br/>

<div align="center">
  
  ### [RNN]
  
  **파일명** : 22_03_25_day09_RNN_Answer.ipynb
  
  ![image](https://user-images.githubusercontent.com/37567501/174435532-015c35c4-e4e3-4c8e-90aa-1ede117e101b.png)
  
</div>

  <br/><br/>
  
  #### RNN 장단점
  
  **[장점]**
  
  : 데이터 관측치가 시간적 순서를 가지고 변수간 상관성이 존재이 존재하는 데이터를 다루며 주로 과거의 데이터를 통해 현재의 움직임과 미래를 예윽하는데 사용합니다.
  
  <br/>
  
  **[단점]**
  
  :정보와 정보 사이의 거리가 멀면 초기의 weight 값이 유지되지 않아 학습 능력이 저하되며 이러한 문제를 장기 의존성 문제 (Long-Term Dependency) 라고 부릅니다.
  
  <br/><br/>
  ---
  <br/><br/>

<div align="center">
  
  ### [LSTM]
  
  **파일명** : 22_03_25_day09_RNN_Answer.ipynb
  
  ![image](https://user-images.githubusercontent.com/37567501/174436482-bdde3a14-54bb-4a96-863d-05b2591fe8f8.png)
  ![image](https://user-images.githubusercontent.com/37567501/174436360-7c10e338-4c71-4135-af90-daaa3197f59b.png)

</div>

  <br/><br/>
  
  #### LSTM 장단점
  
  **[장점]**
  
  : RNN에서 발생하는 기울기 소실(Vanishing Gradient)과 기울기 폭발(Exploding Gradient) 문제를 해결했습니다.
  
  <br/>
  
  **[단점]**
  
  : 연산 속도가 느림며 메모리가 덮어씌워질 가능성이 있습니다.
  
  <br/><br/>
  ---
  <br/><br/>
  
<div align="center">
  
  #### + LSTM_peephole
  
  ![image](https://user-images.githubusercontent.com/37567501/174436764-cfc33413-3936-47a0-9844-4e30cac5c448.png)
  
</div>

  - Felix Gers와 Jurgen Schmidhuber가 게이트 제어기에 장기 상태도 조금 노출시켜 좀 더 많은 문맥을 감지하게 만들면 좋을 수 있다는 아이디어 제안한 모델입니다.


  <br/><br/>
  ---
  <br/><br/>
  
  
<div align="center">
  
  ### [GRU]
  
  **파일명** : 22_03_25_day09_RNN_Answer.ipynb
  
  ![image](https://user-images.githubusercontent.com/37567501/174436580-a76e8428-4bde-45e4-aee9-4c5ea732002c.png)
  
</div>

  - LSTM에 핍홀 연결한 모델에서 hidden state를 업데이트하는 계산을 간소화한 모델입니다.
  


  <br/><br/>
  
  #### GRU 장단점
  
  **[장점]**
  
  : 연산 속도가 빠르며, LSTM처럼 메모리가 덮어씌여질 가능성이 없습니다.
  
  <br/>
  
  **[단점]**
  
  : 메모리와 결과값의 제어가 불가능합니다.
  
  
  <br/><br/>
  ---
  <br/><br/>
  
<div align="center">  
  
  ### [seq2seq]
  
  **파일** : 22_03_28_day10_seq2seq.ipynb
  
  ![](https://aiffelstaticprd.blob.core.windows.net/media/images/GN-4-L-7.max-800x600.jpg)
  
</div>

  일반적인 RNN에서 입력과 출력 시퀀스의 크기는 고정되어 있었습니다. 물론 입력 시퀀스의 크기는 가변적일 수 있기 때문에 이를 동일한 크기의 시퀀스로 만들기 위해 패딩을 했습니다.  미래 한 시점을 예측하는 시계열 문제, 문장으로부터 긍/부정을 예측하는 문제에서는 출력이 하나로 고정되어 있을 것입니다. 
  하지만 앞선 **기계번역 분야에서는 한 언어로 다른 언어로 번역할 때 문장의 길이가 달라질 수 있기 때문에 가변적인 출력 시퀀스에 대한 처리**가 필요할 것입니다.
  이러한 문제를 해결하기 위해 **seq2seq**이 제안되었습니다.

  <br/><br/>
  ---
  <br/><br/>
  
<div align="center"> 
  
  ### [transformer]
  
  **파일명** : 22_03_31_day13_transformer.ipynb, 22_04_01_day14_transformer.ipynb
  
  ![image](https://user-images.githubusercontent.com/37567501/174438067-e61938ec-2404-43dc-9af9-891b21efa787.png)
  
</div>

  seq2seq 모델은 인코더-디코더 구조로 구성되어져 있었습니다. 여기서 인코더는 입력 시퀀스를 하나의 벡터 표현으로 압축하고, 디코더는 이 벡터 표현을 통해서 출력 시퀀스를 만들어냈습니다. 하지만 이러한 구조는 인코더가 입력 시퀀스를 하나의 벡터로 압축하는 과정에서 입력 시퀀스의 정보가 일부 손실된다는 단점이 있었고, 이를 보정하기 위해 어텐션이 사용되었습니다.
  **seq2seq 모델의 단점인 정보 손실 문제를 해결하기 위한 모듈 어텐션 만으로 인코더와 디코더를 구성해보는 모델이 transformer** 입니다.
  
  - [참조](https://wikidocs.net/31379)
  
  <br/><br/>
  ---
  <br/><br/>
  
<div align="center"> 
  
  ### [huggingface & BERT]
  
  **파일명** : 22_04_05_day15_huggingface_tutorial.ipynb, 22_04_06_day16_huggingface_pretrained.ipynb
  
</div>
  
  <br/><br/>
  
  **[huggingface]**
  
  : 트랜스포머를 기반으로 하는 다양한 모델(transformer.models)과 학습 스크립트(transformer.Trainer)를 구현해 놓은 모듈입니다.
  
  <br/>
  
  **[BERT]**
  
  : BERT는 사전 학습된 대용량의 레이블링 되지 않는(unlabeled) 데이터를 이용하여 언어 모델(Language Model)을 학습하고 이를 토대로 특정 작업( 문서 분류, 질의응답, 번역 등)을 위한 신경망을 추가하는 전이 학습 방법입니다.
  
![Footer](https://capsule-render.vercel.app/api?type=waving&color=gradient&height=200&section=footer)

