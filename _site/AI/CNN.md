# CNN(Convolutional Neural Network)
### CNN을 사용하는 이유
* fully-connected 계층을 사용하면 데이터의 형상이 고려되지 않는다. (3차원의 데이터를 1차원으로)
* CNN은 데이터의 형상을 유지하여 연산을 진행한다.
### Convolutional Layer
* filter = kernel -> weight에 해당하는 것
* 필터 연산을 진행 => 필터의 개수는 layer별 연산시간량을 일정하게 유지할 수 있도록 정한다
* pooling이 2*2라면 픽셀은 1/4 줄어들게 된다 => 필터의 개수는 4배 증가시킨다
* n * n 의 input data가 m * m 의 kernel을 만나면 n-(m-1) * n - (m-1)의 output이 된다. (padding=0, stride=1 일때)
* padding: input data에 특정한 값으로 채워서 output의 크기를 조절한다.
* stride: 필터 연산의 간격
### Pooling Layer
* pooling size = n이라면 input data의 n*n 영역을 하나의 영역으로 줄이는 것
* max pooling이라면 일정한 크기 내에서 가장 큰 값을 뽑아내는 것으로 이미지의 특징을 추출하고 overfitting을 줄일 수 있다.
* max pooing, average pooling 등이 있으며 이미지 인식 분야에서는 주로 max pooling 사용
## Lenet-5
* 손글씨를 인식하기 위한 nn으로 1998년에 고안되었다.
* 2개의 convolutional layer와 2개의 pooling(subsampling) layer와 full connection layer로 이루어져 있다.
* input은 32*32의 픽셀 이미지
* C1 layer: kernel은 6개, kernel_size=5, stride=1으로 input(1*32*32) -> output(6*28*28)
* S2 layer: pooing_size = 2, stride = 2 input(6*28*28) -> output(6*14*14)
* C3 layer: kernel은 16개, kernel_size=5, stride=1으로 input(6*14*14) -> output(16*10*10)
* S4 layer: pooing_size = 2, stride = 2 input(16*10*10) -> output(16*5*5)
* C5 layer: kernel은 120개, kernel_size=5, stride=1으로 input(16*5*5) -> output(120*1*1)
* F6 layer: dot product input(120) -> output(84)
* output layer: input(84) -> output(10)
* https://ieeexplore.ieee.org/document/726791

## 그외
* AlexNet
* VGGNet
* ZFNet
* GoogLeNet,
* ResNet
* DenseNet
* ShuffleNet
