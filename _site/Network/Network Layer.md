# Network Layer
## Fucntions
### 1. forwarding
* 패킷을 라우터의 input link interface에서 적절한 output link interface로 옮기는 것
* forwarding table을 사용
* HW로 구현(Data plane)
### 2. routing
* 출발지에서 도착지까지의 패킷의 route를 결정
* forwarding table을 설정
* routing algorithm(Dijkstra's, Bellman-Ford 등)
* SW로 구현(Control plane)
## Input/Ouput port
### Input port
> forwarding
> * destination-based forwarding
> * generalized forwarding

> queuing
> * datagram이 switch fabric에 forwarding rate보다 빨리 도착하면 발생
> * 아직 앞의 packet의 forwarding이 이루어지지 않았다면? -> queuing delay 발생
### Output port
* Output port는 output port의 메모리에 저장된 패킷을 output link로 전송한다.
> buffering
> * datagram이 fabric에서 transmission rate보다 빨리 도착할 때 발생
> * RTT*C/&radic;N
> * link capacity C, N flows
> * Rule of thumb: 평균 buffering은 RTT와 link capacity의 곱

> scheduling
> * FIFO scheduling
> * Priority scheduling
> * Round Robin scheduling
> * Weighted Fair Queuing
