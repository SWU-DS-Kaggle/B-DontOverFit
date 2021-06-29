# B-DontOverFit

### 😍수민
 
 #### shap이란?
- 블랙박스 모델의 예측 결과를 설명하기 위한 매소드이다. 
 최근에 많이 쓰는 DNN, 로지스틱, 그래디언트 부스팅 모델등은 블랙박스 모델인데, 이러한 모델에서 결과를 해석하고 '왜'이러한 결과가 나왔는지 설명해주기 위하여 shap같은 메소드를 사용한다. 

 #### 유래?
 - 게임이론 중 shapley values에 기초하여 나왔다. 
shapley values는 각 공헌자가 얼마나 공헌했는지 나타내는 수치이다. 협력과 비협력에 따른 영향을 계산한다. 

 #### 문제점? 
 - 변수간 높은 상관관계에 취약하다 

 참고) https://shap-lrjball.readthedocs.io/en/latest/index.html
 
 
 
### 😍혜빈
eli5: 항목의 중요도를 보여주고 의사결정 트리, 트리기반 앙상블 예측, 각 항목이 최종 결과에 얼마나 기여했는지
=> 데이터에서 영향력이 없는 것은 빼는 과정
블랙박스: 알고리즘이 뭔가를 넣으면 결과가 나오지만 무슨 일이 일어나는지 모를 때 <-> 왜 이런 결과가 나왔는지 볼 수 있게 어떤 항목이 중요했는지를 볼 수 있다. 

### 😍민지

### 😍성윤

keywords : default parameter -> select best features -> run grid search -> train best model -> feature selection of each models

models used : Logistic Regression, AdaBoost Classifier, SGD Classifier, SVC

![image](https://user-images.githubusercontent.com/81219515/123797194-e63efa80-d920-11eb-836c-1c3e21bc8f33.png)

![image](https://user-images.githubusercontent.com/81219515/123797236-f1922600-d920-11eb-9fdc-f3832a4cf7ed.png)
