# B-DontOverFit

### ๐์๋ฏผ
 
 #### shap์ด๋?
- ๋ธ๋๋ฐ์ค ๋ชจ๋ธ์ ์์ธก ๊ฒฐ๊ณผ๋ฅผ ์ค๋ชํ๊ธฐ ์ํ ๋งค์๋์ด๋ค. 
 ์ต๊ทผ์ ๋ง์ด ์ฐ๋ DNN, ๋ก์ง์คํฑ, ๊ทธ๋๋์ธํธ ๋ถ์คํ ๋ชจ๋ธ๋ฑ์ ๋ธ๋๋ฐ์ค ๋ชจ๋ธ์ธ๋ฐ, ์ด๋ฌํ ๋ชจ๋ธ์์ ๊ฒฐ๊ณผ๋ฅผ ํด์ํ๊ณ  '์'์ด๋ฌํ ๊ฒฐ๊ณผ๊ฐ ๋์๋์ง ์ค๋ชํด์ฃผ๊ธฐ ์ํ์ฌ shap๊ฐ์ ๋ฉ์๋๋ฅผ ์ฌ์ฉํ๋ค. 

 #### ์ ๋?
 - ๊ฒ์์ด๋ก  ์ค shapley values์ ๊ธฐ์ดํ์ฌ ๋์๋ค. 
shapley values๋ ๊ฐ ๊ณตํ์๊ฐ ์ผ๋ง๋ ๊ณตํํ๋์ง ๋ํ๋ด๋ ์์น์ด๋ค. ํ๋ ฅ๊ณผ ๋นํ๋ ฅ์ ๋ฐ๋ฅธ ์ํฅ์ ๊ณ์ฐํ๋ค. 

 #### ๋ฌธ์ ์ ? 
 - ๋ณ์๊ฐ ๋์ ์๊ด๊ด๊ณ์ ์ทจ์ฝํ๋ค 

 ์ฐธ๊ณ ) https://shap-lrjball.readthedocs.io/en/latest/index.html
 
 
 
### ๐ํ๋น
eli5: ํญ๋ชฉ์ ์ค์๋๋ฅผ ๋ณด์ฌ์ฃผ๊ณ  ์์ฌ๊ฒฐ์  ํธ๋ฆฌ, ํธ๋ฆฌ๊ธฐ๋ฐ ์์๋ธ ์์ธก, ๊ฐ ํญ๋ชฉ์ด ์ต์ข ๊ฒฐ๊ณผ์ ์ผ๋ง๋ ๊ธฐ์ฌํ๋์ง
=> ๋ฐ์ดํฐ์์ ์ํฅ๋ ฅ์ด ์๋ ๊ฒ์ ๋นผ๋ ๊ณผ์ 
๋ธ๋๋ฐ์ค: ์๊ณ ๋ฆฌ์ฆ์ด ๋ญ๊ฐ๋ฅผ ๋ฃ์ผ๋ฉด ๊ฒฐ๊ณผ๊ฐ ๋์ค์ง๋ง ๋ฌด์จ ์ผ์ด ์ผ์ด๋๋์ง ๋ชจ๋ฅผ ๋ <-> ์ ์ด๋ฐ ๊ฒฐ๊ณผ๊ฐ ๋์๋์ง ๋ณผ ์ ์๊ฒ ์ด๋ค ํญ๋ชฉ์ด ์ค์ํ๋์ง๋ฅผ ๋ณผ ์ ์๋ค. 

### ๐๋ฏผ์ง
### "๊ต์ฐจ๊ฒ์ฆ"
cross validation
: ๋ฐ์ดํฐ ๊ฐ์๊ฐ ์ ์๋ fold out ํ๊ฐ์ ๋ฎ์ ์ ๋ขฐ์ฑ ๋ฌธ์ ๋ฅผ ํด๊ฒฐํ๊ธฐ ์ํด์ ํ๋ จ ๋ฐ์ดํฐ ์๊ณผ ํ์คํธ ๋ฐ์ดํฐ ์์ ์ฌ๋ฌ๋ฒ ๋ง๋ค์ด ํ์ต-์์ธก์ ์ฌ๋ฌ๋ฒ ์ํํ๊ณ  ํ๊ท  ์ ํ๋๋ฅผ ๊ตฌํ๋ ํ๊ฐ๋ฐฉ์
-> ๊ต์ฐจ๊ฒ์ฆ์ ํตํด ์ข ๋ ์ ๋ขฐ์ฑ์๋ ๊ฒ์ฌ๋ฅผ ํ  ์ ์๋ค

<์ข๋ฅ>
1. k-fold cross validation
2. shuffle split cross validation
3. leave-one-out cross validation
4. leave-p-out cross validation

![์บก์ฒ](https://user-images.githubusercontent.com/68270424/123816027-f01d2980-d931-11eb-895f-dc21d1f6a2ed.PNG)

### k fold
### k=5์ผ๋ ๋๋ค์ผ๋ก ํธ๋ ์ธ ์ธํธ๋ฅผ 5์กฐ๊ฐ์ผ๋ก ๋๋์ด 4๊ฐ๋ ํธ๋ ์ธ์ฉ 1๊ฐ๋ ๊ต์ฐจ๊ฒ์ฆ์ฉ์ผ๋ก ์ฌ์ฉ

### k fold cross validation 
### k ํด๋ ๊ต์ฐจ ๊ฒ์ฆ
k=5, 5์ธํธ๋ฅผ ๋ง๋ค๋ฉด 4์ธํธ๊ฐ ํ์ต ๋ฐ์ดํฐ(train ์ฉ)๊ฐ ๋๊ณ  5๋ฒ์งธ ์ธํธ๋ ์ ํจ์ฑ ๊ฒ์ฌ(๊ต์ฐจ ๊ฒ์ฆ์ฉ)๋ฅผ ์ํ๊ฒ 

k
k-1 -> ํธ๋ ์ธ ์
1 -> ํ์คํธ ์
k๋ฒ ํ์๋งํผ ๊ต์ฐจ๊ฒ์ฆ์ ๋ฐ๋ณต
k=5๋ฉด ์ ํ๋๊ฐ 5๊ฐ -> ๊ทธ๊ฑฐ์ ํ๊ท 


kFold์์ ๋๋ ๋ถ๋ถ์ด ํธํฅ๋  ์ ์์ผ๋ฏ๋ก 
์ฌ์ง์ฒ๋ผ ์ฌ๊ธฐ์ ๊ธฐ์ ์์งํจ

์ผ๋ฐ์ ์ผ๋ก kFold๋ ํ๊ท์์ ์ฌ์ฉํ๊ณ 
startifiedKFold๋ ๋ถ๋ฅ์ ์ฌ์ฉ๋๋ค

![star](https://user-images.githubusercontent.com/68270424/123816070-f9a69180-d931-11eb-8ab0-8ed24751dc25.PNG)

### startified K Fold
๊ณ์ธตํ k๊ฒน ๊ต์ฐจ๋ฑ๊ธ
: ๊ณ์ธตํ๋ ํด๋๋ฅผ ๋ฐํํ๋ k ํด๋์ ๋ณํ์ด๋ค
-> ๋ฐ์ดํฐ๊ฐ ํธํฅ๋๋ฉด k ํด๋ ๊ต์ฐจ ๊ฒ์ฆ์ด ์ ๋๋ก ์ํ๋์ง ์์ ์ ์๋ค -> ๊ทธ๋์ ํธ๋ ์ธ ์ธํธ์ ์ ํจ์ฑ ๊ฒ์ฌ ์ธํธ๋ฅผ ์ฌ๊ธฐ์ ๊ธฐ์ ์์งํจ

๊ฐ์ธํธ์๋ ๊ฐ ์ธํธ์ ์ํ์ด ์ ์ฒด ์ธํธ์ ๊ฑฐ์ ๊ฐ์ ๋น์จ๋ก ํฌํจ๋์ด์์


![g](https://user-images.githubusercontent.com/68270424/123816112-01663600-d932-11eb-8aa3-366433e4416e.PNG)

### Repeated Stratified K Fold
: startifiedKFold์ ๋น์ทํจ ์๋ ๊ทธ ์์์ ๋ฐ๋ณต๋จ
-> ๊ฐ ๋ฐ๋ณต๋ง๋ค ๋ ๋๋ค์ผ๋ก n๋ฒ ๋ฐ๋ณต
"๊ต์ฐจ๊ฒ์ฆ ๋ด๋ถ์ ๊ต์ฐจ๊ฒ์ฆ์ด ์๋ค"



### ๐์ฑ์ค

keywords : default parameter -> select best features -> run grid search -> train best model -> feature selection of each models

models used : Logistic Regression, AdaBoost Classifier, SGD Classifier, SVC

![image](https://user-images.githubusercontent.com/81219515/123797194-e63efa80-d920-11eb-836c-1c3e21bc8f33.png)

![image](https://user-images.githubusercontent.com/81219515/123797236-f1922600-d920-11eb-9fdc-f3832a4cf7ed.png)
