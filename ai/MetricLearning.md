# Metric Learning, Deep Metric Learning (DML)
------
## 개요
Metric learning은, 데이터에 적합한 distance function을 학습하는 분야이다.

Deep Metric Learning은, 신경망을 사용하여 metric learning을 하는 분야이다. 일반적으로 embedding space에서 Euclidean distance를 사용하므로, 결국은 데이터에 잘 맞는 embedding function을 학습하는 것이 목적이 된다.


## 종류

### Constrative Embedding
2개의 샘플에 대해 적용한다. 

각각의 tuple (**x**<sub>i</sub>, **x**<sub>j</sub>, y<sub>ij</sub>)에 대해 같은 class이면 가깝게, 다른 class이면 멀게 되도록 embedding ft.을 학습한다. '멀게'의 유효 최대치는 hyperparameter인 𝞪로 설정한다.


### Triplet Embedding
3개의 샘플(anchor sample, positive sample, negative sample)에 대해 적용한다.

(anchor와 positive 간의 거리)와 (anchor와 negative 간의 거리)의 차이가 크게 되도록 학습한다.


### Log-Ratio Embedding
앞의 두 개는 분류(classification) 문제, 즉 discrete 형태의 문제에 적용할 수 있는 것이다. Regression과 같이 연속적인 값을 목표로 하는 경우에 적용할 수 있도록 한 방법이다.

(anchor 샘플과 positive 샘플 간의 거리)와 (anchor 샘플과 negative 샘플 간의 거리)의 log-ratio가, <br>
(anchor 목표값과 positive 목표값 간의 거리)와 (anchor 목표값과 negative 목표값 간의 거리)의 log-ratio와 가깝게 되도록 학습한다.
