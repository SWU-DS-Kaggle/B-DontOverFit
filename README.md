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
### "교차검증"
cross validation
: 데이터 개수가 적을때 fold out 평가의 낮은 신뢰성 문제를 해결하기 위해서 훈련 데이터 셋과 테스트 데이터 셋을 여러번 만들어 학습-예측을 여러번 수행하고 평균 정확도를 구하는 평가방식
-> 교차검증을 통해 좀 더 신뢰성있는 검사를 할 수 있다

<종류>
1. k-fold cross validation
2. shuffle split cross validation
3. leave-one-out cross validation
4. leave-p-out cross validation

![캡처](https://user-images.githubusercontent.com/68270424/123816027-f01d2980-d931-11eb-895f-dc21d1f6a2ed.PNG)

### k fold
### k=5일때 랜덤으로 트레인 세트를 5조각으로 나누어 4개는 트레인용 1개는 교차검증용으로 사용

### k fold cross validation 
### k 폴드 교차 검증
k=5, 5세트를 만들면 4세트가 학습 데이터(train 용)가 되고 5번째 세트는 유효성 검사(교차 검증용)를 위한것 

k
k-1 -> 트레인 셋
1 -> 테스트 셋
k번 횟수만큼 교차검증을 반복
k=5면 정확도가 5개 -> 그거의 평균


kFold에서 나눈 부분이 편향될 수 있으므로 
사진처럼 여기저기서 수집함

일반적으로 kFold는 회귀에서 사용하고
startifiedKFold는 분류에 사용된다

![star](https://user-images.githubusercontent.com/68270424/123816070-f9a69180-d931-11eb-8ab0-8ed24751dc25.PNG)

### startified K Fold
계층화 k겹 교차등급
: 계층화된 폴드를 반환하는 k 폴드의 변형이다
-> 데이터가 편향되면 k 폴드 교차 검증이 제대로 수행되지 않을 수 있다 -> 그래서 트레인 세트와 유효성 검사 세트를 여기저기서 수집함

각세트에는 각 세트의 샘플이 전체 세트와 거의 같은 비율로 포함되어잇음


![g](https://user-images.githubusercontent.com/68270424/123816112-01663600-d932-11eb-8aa3-366433e4416e.PNG)

### Repeated Stratified K Fold
: startifiedKFold와 비슷함 얘는 그 안에서 반복됨
-> 각 반복마다 또 랜덤으로 n번 반복
"교차검증 내부에 교차검증이 있다"



### 😍성윤

keywords : default parameter -> select best features -> run grid search -> train best model -> feature selection of each models

models used : Logistic Regression, AdaBoost Classifier, SGD Classifier, SVC

![image](https://user-images.githubusercontent.com/81219515/123797194-e63efa80-d920-11eb-836c-1c3e21bc8f33.png)

![image](https://user-images.githubusercontent.com/81219515/123797236-f1922600-d920-11eb-9fdc-f3832a4cf7ed.png)
