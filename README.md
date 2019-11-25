# Kaggle-Titanic
## 문제정의
이 대회는 많은 사람을 죽음으로 몰고 간 `Titanic 호 침몰 사건`을 주제로 다룬다.</br>
생존에 영향을 미친 여러 요인이 있겠지만, 대회에서 주어진 Train 승객들의 정보만으로 Test 승객들의 생존 여부를 예측하는 대회이다.</br>
생존과 연루되어 있다고 생각되는 몇 가지의 요소들에 대해 분석하여 어떤 조건을 갖춘 그룹들이 생존할 확률이 더 높았는지에 대해 알아보려고 한다.


</br>
Titanic 승객에 대한 정보는 다음과 같이 주어진다.

- PassengerId

- Sex

- Age

- Parch

- Pclass

- Ticket

- Embarked

- Cabin

- Name

- SibSp

- Fare

- Survived(train에만)

</br></br>
여기서 내가 해야할 것은 다음과 같다.


1. Cabin은 '알파벳+숫자'로 구성되어있다. 따라서 알파벳별로 객실을 분류하여 비교분석할 것이다.

2. Name에서 칭호(Mr, Miss, Master 등)를 분리하고, 칭호별로 분류하여 비교분석할 것이다.

3. Fare와 Pclass의 관계를 알아내고, Pclass만 활용해도 되는지 알아낼 것이다.

4. SibSp, Parch 그리고 SibSp+Parch 이 세가지 경우를 비교분석할 것이다.

5. Ticket번호의 길이, 알파벳 유무(only 숫자인 경우, 알파벳+숫자인 경우가 있다.)가 혹시나 생존여부에 영향을 미치지 않는지 분석해볼 것이다.

5-1. 4번과 겹칠 수 있지만, 여러명이 같은 Ticket번호(아마 가족관계일듯)를 가지고 있다면, 해당 번호를 가진 사람들은 그렇지 않은 사람들에 비해 생존확률이 높은지 확인해보고 싶다.

6. 승선한 항구(Embarked)명에 따라 비교분석할 것이다.

7. 성별에 따라 비교분석할 것이다.

8. 나이에 따라 비교분석할 것이다. 

8-1. 나이 정보가 누락된 사람들은, mean 또는 median으로 채워볼 것이고, 다른 정보로 나이를 예측해보기도 할 것이다.
