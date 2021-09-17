# Entropy 개념
* 불확실성을 측정하는 방법이다. - > $H$
* 불확실성이 커진다면 entropy의 크기도 커진다.
# Cross Entropy Error
* loss function으로 사용한다.</br>
$$
E = \sum_{k=1}^n t_klog_y_k
$$</br>
$t_k$는 label, $y_k$는 신경망의 output
