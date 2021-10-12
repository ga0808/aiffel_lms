# aiffel_lms


#### 과제물 평가항목
1. 이미지 분류기 모델이 성공적으로 만들어졌는가?   
:트레이닝이 정상적으로 수행되었음  

2. 오버피팅을 극복하기 위한 적절한 시도가 있었는가?  
:데이터셋의 다양성, 정규화 등의 시도가 적절하였음

3. 분류모델의 test accuracy가 기준 이상 높게 나왔는가?  
:60% 이상 도달하였음

#### 스스로 생각한 평가
1. 트레이닝이 정상적으로 수행되었는가  
-> 스스로 판단하기 어려움  
정확도를 보더라도 1.0은 나오지만   
정확도가 너무 가파르다고 생각되어서 뭔가 잘못된것 같고    
테스트는 처음부터 너무 높은 정확도가 나옴  
과적합인지 아닌지, 좋은 학습이 되었는지에 대해서 판단하는 통찰이 부족함  

2. 오버피팅을 위한 시도  
->1500개 학습 데이터+ 300개 검증 데이터로 데이터 다양화함  
정규화도 시도함

3.60% 이상의 정확도  
->train, val, test 모두 100%의 정확도에 도달함  
(도달 하긴함.. 근데 도달만 해서 의미가 있는건지 모르겠음)  

#### 정확도에 대한 견해
1. train

![image](https://user-images.githubusercontent.com/90363244/135453284-bfa79936-78ba-4540-8ce5-f6a312470df7.png)

첫번째 정확도 0.3, 마지막엔 1.0도달  
-> 처음부터 높은 정확도가 나오지 않음  
-> 오버피팅이 아니다...! (아마도ㅎㅎ) 
 *강민님 깃헙 보니까, 첨부터 너무 높은 정확도 나오면 오버피팅이라고 하시는 것 같음  
 오버피팅,언더피팅 여부를 알 수 있는 것은 plot 그려서 보는것 말고 또 다른 지표가 있는지 공부해보기*

2. validation 

![image](https://user-images.githubusercontent.com/90363244/135453722-06820c57-8f64-4dc2-8fed-52bd1143a3b0.png)

-> 정확도가 너무 높지않게 시작  
*그런데 너무 정확도가 가파르게 오르는 경향이 있음  
: train도 안그럴때도 있지만, 그럴때가 더 많은 것으로 관찰되는 편  
-> 이유가 무엇인지, 어떻게 개선해야하는지 등에 대한 여부 더 공부해볼점*

3. test
 
![image](https://user-images.githubusercontent.com/90363244/135454756-bc5478cc-bb63-4260-a1c5-c23d2767f394.png)

0.9부터 시작되어 높은 정확도라 판단되어 과적합인가 싶음
-> 그런데 강민님의 다섯번째 트라이를 보니까  
-> 0.9로 정확도가 시작되지만 상승되었고+ 오버피팅 아니라고 판단하심

#### 회고
정확도가 1.0이 나오긴 했지만, 정확도만 보고 모델을 신뢰하기에는 역부족이었던 것같음
스스로에 대해서 신뢰가 없어서 정확도 수치에도 의심이 가는건지 모르겠지만
쨋든 정확도를 보고, 모델을 평가하고 판단할 수 있을 만큼 좀 더 공부하고 
plot 그려보고 하면서 좀 더 전체적인 인사이트를 얻을 수 있도록 해야함... ㅠ