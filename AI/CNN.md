# CNN(Convolutional Neural Network)
### CNN을 사용하는 이유
* fully-connected 계층을 사용하면 데이터의 형상이 고려되지 않는다. (3차원의 데이터를 1차원으로)
* CNN은 데이터의 형상을 유지하여 연산을 진행한다.
### Convolutional Layer
* filter = kernel -> weight에 해당하는 것
* 필터 연산을 진행
* n * n 의 input data가 m * m 의 kernel을 만나면 n-(m-1) * n - (m-1)의 output이 된다. (padding=0, stride=1 일때)
* padding: input data에 특정한 값으로 채워서 output의 크기를 조절한다.
* stride: 필터 연산의 간격
### Pooling Layer
* pooling size = n이라면 input data의 n*n 영역을 하나의 영역으로 줄이는 것
* max pooing, average pooling 등이 있으며 이미지 인식 분야에서는 주로 max pooling 사용
