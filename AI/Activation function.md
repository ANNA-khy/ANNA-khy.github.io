# Activation function
* 인공지능 신경망에서 입력이 주어졌을 때 출력을 내는 함수

# Sigmoid funtcion
* 자주 활용되는 activation function
* x의 값이 커지면 $\exp (-x)$는 $-infinity$로 가고 x의 값이 작아지면 0으로 간다.
* sigmoid function은 x의 값이 커지면 0에 수렴하고 x의 값이 0에 가까워지면 1에 수렴한다.
$$ h(x) = {1 \over 1+\exp (-x)} $$
