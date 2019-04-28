# 2019.04.28_Classifying_Dogs

Classifying Shiba and Jindo dog with keras
시바견과 진돗개를 구분해보자!

데이터셋은 직접 크롤러를 통해서 네이버,구글에서 수집하였다. 

전처리는 openCV를 이용해서 resize, normalization 등을 거쳤다. 
Network는 Keras를 이용해서 쌓았고, 다양한 Optimizers를 이용했다.

하지만 육안으로도 구별하기 힘든 것으로 미루어 봤을 때, 성능이 잘 안나오는 것 같다. 그렇다고 여기서 포기하지는 않고, 다음의 계획을 세웠다.

* 각 클래스당 10,000장을 확보하자

데이터가 부족해서인지 Overfitting이 자주나고 성능이 계속적으로 좋지 않았다. 

* Color scale로 다시 분석하기

정보를 최대한 잃지 않는 방법을 택하기로 했다. 먼저 기존에 grayscale로 설정했던 이유는, 진돗개와 시바견의 색상이 한 가지가 아니었기 때문이다. 
그래서 오히려 분류하는데 방해가 될 것이라고 판단해서 grayscale로 변환 후 분석했다. 실제도 Stanford dog breed classification에서도 grayscale을 사용했다. 

* Pre-trained Network 이용

VGG Net, Inception-v3, ResNet등 기존에 학습된 networks를 이용해서 Transfer learing을 할 것 이다. 

정제된 데이터를 얻기가 힘들기 때문에 시간을 가지고 데이터를 수집하고, 정제하고 다시 분석하는 시간을 가질 것 이다!!
