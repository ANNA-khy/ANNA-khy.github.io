# Entropy 개념
* 불확실성을 측정하는 방법이다. - > $H$
* 불확실성이 커진다면 entropy의 크기도 커진다.
# Cross Entropy Error
* loss function으로 사용한다.</br>
<math>
$$E = \sum_{k} t_k \log{y_k}$$
  </br>
</math>
($t_k$는 label, $y_k$는 신경망의 output)
