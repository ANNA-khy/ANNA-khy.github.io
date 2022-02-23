# Timeout
* TimeoutInterval = EstimatedRTT + 4*DevRTT
* DevRTT는 RTT 값이 다양한 분포를 가지므로 이를 고려한 margin이다.
# EstimatedRTT
* EstimatedRTT = (1-alpha)*EstimatedRTT(이전 값) + (alpha)*SampleRTT(가장 최근에 측정된 RTT)
* alpha는 보통 0.125
# DevRTT
* DevRTT = (1-beta)*DevRTT(이전 값) + (beta)*(SampleRTT-EstimatedRTT)의 절대값
* beta는 보통 0.25
