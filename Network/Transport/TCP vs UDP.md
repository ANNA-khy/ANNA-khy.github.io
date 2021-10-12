# TCP(Transmission Control Protocol)
* 신뢰성 있는 데이터 전송 => 100% 데이터 전송 or 0% (fail)
* 연결 전 데이터 전송을 위한 setup 과정이 존재
* in-order delivery
* 혼잡 제어, 흐름 제어 기능이 있음
* 이메일 전송 등에 사용
# UCP(User Datagram Protocol)
* 신뢰할 수 없는 데이터 전송
* unordered delivery
* 혼잡 제어, 흐름 제어 기능이 없음
* TCP보다 간단하며 overhead도 적다.
* 실시간 화상 미팅 등에 사용

# Both
* multiplexing 및 demultiplexing
* checksum을 이용하여 error를 확인
