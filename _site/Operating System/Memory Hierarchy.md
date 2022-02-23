# Memory Hierarchy
## 계층구조 특징
> 낮은 hierarchy로 갈수록
> * bit당 비용 감소
> * 용량(capacity) 증가
> * 접근 시간(access time) 증가
> * 프로세서에 의해 메모리로 접근하는 빈도가 줄어듦
## Locality of reference
> 프로그램이 loop나 subroutine으로 들어가면 명령들이 반복되어 참조(reference)된다.(시간적)
> </br>프로그램이 table이나 array로 된 연산을 수행할 때 군집화된(clustered) 데이터에 접근한다.(공간적)
## 계층구조
### 1. Registers
* 프로세서가 현재 수행 중인 연산에 사용되는 값들이 저장됨
* Instruction register, Memory address register(다음에 메모리에 읽거나 쓸 주소), Memory buffer register(메모리에 쓰여질 데이터), Input/out address register, Input/output buffer register
### 2. Cache
* Tag와 Block(K words 크기)으로 이루어짐
* C개의 슬롯으로 이루어짐
* mapping function: 캐시 안에서 각 block의 위치
* replacement algorithm, write policy을 적절하게 정하는 것이 중요
### 3. Main memory
### 4. Magnetic disk
### 5. Magnetic tape 
