---
title: Activation Function
use_math: true
---
# Activation function
* 인공지능 신경망에서 입력이 주어졌을 때 출력을 내는 함수

## Sigmoid funtcion
* 자주 활용되는 activation function
* x의 값이 커지면 $\exp (-x)$는 $-infinity$로 가고 x의 값이 작아지면 0으로 간다.
* sigmoid function은 x의 값이 커지면 0에 수렴하고 x의 값이 0에 가까워지면 1에 수렴한다.
$$ h(x) = {1 \over 1+\exp (-x)} $$

## Softmax function
* 분류에 많이 사용하는 activation function
* 출력의 총합은 1
$$ y_k = \frac{\exp (a_k)}{\sum_{i=1}^n \exp (a_i)}$$

## ReLU function
* Rectified Linear Unit function
* 자주 활용되는 activation function
* 입력이 0을 넘으면 그 입력 값을 그대로 출력하고 0이하이면 0을 출력
$$ h(x) = 
\begin{cases}
x & (x>0) \\\\
0 & (x\le0)
\end{cases} $$
