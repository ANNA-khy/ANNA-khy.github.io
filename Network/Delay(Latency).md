# Delay
### 1. nodal processing
* bit error를 체크
* 어떤 output link로 가야할 지 결정
* < msec
### 2. queueing delay
* output link에서 패킷이 전송(transmission)되기를 기다리는 시간
* 라우터의 혼잡도와 관련있음
* 종종 delay의 주요한 원인
### 3. transmission delay
* 패킷의 모든 bit가 라우터의 link로 보내는데(push) 걸리는 시간
* packet length(L: bits)/link bandwidth(R: bps)
* d<sub>trans</sub> = L/R
### 4. propagation delay
* 하나의 bit가 하나의 end에서 다른 end로 travel하는 데 걸리는 시간
* D: length of physical link
* s: propagation speed
* d<sub>prop</sub> = D/s
* packet의 길이와 transmission rate와 관련이 없음

## Delay performance
* one bit 전송 -> propagation delay가 중요
* 패킷의 크기가 큼 -> bandwidth이 중요(transmission delay가 중요)
