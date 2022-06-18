<div align="center">
  
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=200&section=header&text=NLP&fontSize=50" />
  
  ### [RNN]
  
  파일명 : 22_03_25_day09_RNN_Answer.ipynb
  
  ![image](https://user-images.githubusercontent.com/37567501/174435532-015c35c4-e4e3-4c8e-90aa-1ede117e101b.png)
  
</div>

  <br/><br/>
  
  #### RNN 장단점
  
  **[장점]**
  
  : 데이터 관측치가 시간적 순서를 가지고 변수간 상관성이 존재이 존재하는 데이터를 다루며 주로 과거의 데이터를 통해 현재의 움직임과 미래를 예윽하는데 사용
  
  <br/>
  
  **[단점]**
  
  :정보와 정보 사이의 거리가 멀면 초기의 weight 값이 유지되지 않아 학습 능력이 저하되며 이러한 문제를 장기 의존성 문제 (Long-Term Dependency) 라고 부름
  
  <br/><br/>
  ---
  <br/><br/>

<div align="center">
  
  ### [LSTM]
  
  파일명 : 22_03_25_day09_RNN_Answer.ipynb
  
  ![image](https://user-images.githubusercontent.com/37567501/174436482-bdde3a14-54bb-4a96-863d-05b2591fe8f8.png)
  ![image](https://user-images.githubusercontent.com/37567501/174436360-7c10e338-4c71-4135-af90-daaa3197f59b.png)

</div>

  <br/><br/>
  
  #### LSTM 장단점
  
  **[장점]**
  
  : RNN에서 발생하는 기울기 소실(Vanishing Gradient)과 기울기 폭발(Exploding Gradient) 문제를 해결
  
  <br/>
  
  **[단점]**
  
  : 연산 속도가 느림며 메모리가 덮어씌워질 가능성이 있
  
  <br/><br/>
  ---
  <br/><br/>
  
<div align="center">
  
  #### LSTM 핍홀
  
  ![image](https://user-images.githubusercontent.com/37567501/174436764-cfc33413-3936-47a0-9844-4e30cac5c448.png)
  
  - Felix Gers와 Jurgen Schmidhuber가 게이트 제어기에 장기 상태도 조금 노출시켜 좀 더 많은 문맥을 감지하게 만들면 좋을 수 있다는 아이디어 제안
  
</div>

  <br/><br/>
  ---
  <br/><br/>
  
  
<div align="center">
  
  ### [GRU]
  
  파일명 : 22_03_25_day09_RNN_Answer.ipynb
  
  ![image](https://user-images.githubusercontent.com/37567501/174436580-a76e8428-4bde-45e4-aee9-4c5ea732002c.png)
  
  - LSTM에 핍홀 연결한 모델에서 hidden state를 업데이트하는 계산을 간소화한 것이 GRU이다.
  
</div>

  <br/><br/>
  
  #### GRU 장단점
  
  **[장점]**
  
  : 연산 속도가 빠르며, LSTM처럼 메모리가 덮어씌여질 가능성이 없음
  
  <br/>
  
  **[단점]**
  
  : 메모리와 결과값의 제어가 불가능
  
  
  <br/><br/>
  ---
  <br/><br/>
  
  
  ### [seq2seq]
  <img src=https://user-images.githubusercontent.com/37567501/174423209-69e83f82-3846-48f3-901e-20f40ec46e4a.png width="850" height="400"/>
  
  <br/><br/>
  ---
  <br/><br/>
  
  ### [transformer]
  <img src=https://user-images.githubusercontent.com/37567501/174423209-69e83f82-3846-48f3-901e-20f40ec46e4a.png width="850" height="400"/>
  
  <br/><br/>
  ---
  <br/><br/>
  
  ### [huggingface]
  <img src=https://user-images.githubusercontent.com/37567501/174423209-69e83f82-3846-48f3-901e-20f40ec46e4a.png width="850" height="400"/>
  
  
  ![Footer](https://capsule-render.vercel.app/api?type=waving&color=gradient&height=200&section=footer)

