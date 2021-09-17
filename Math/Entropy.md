# Entropy 개념
* 불확실성을 측정하는 방법이다. - > $H$
* 불확실성이 커진다면 entropy의 크기도 커진다.
* random variable들의 분포가 넓게 퍼져있다면 entropy 값은 커지고 좁게 분포하고 있다면 entropy 값은 작아진다.
# Cross Entropy Error
* loss function으로 사용한다.</br>
$$E = \sum_{k} t_k \log{y_k}, (t_k = label, y_k = 신경망의 output)$$
</br>
* entropy 값이 크다 -> loss가 크다
* entropy 값이 작다 -> loss가 적다
