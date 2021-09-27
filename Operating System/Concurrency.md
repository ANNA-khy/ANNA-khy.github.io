# Key Terms
## Atomic operation
* 다른 프로세스가 이 operation에 interrupt를 걸 수 없다.
* 그룹 단위에 실행되는 것을 보장받거나 아예 실행하지 않는다.
## Critical section
* 프로세스의 코드 안에서 공유된 자원에 접근하는 부분으로 한 프로세스가 이 부분을 실행하고 있으면 다른 프로세스는 이 부분을 실행하지 말아야 한다.
## Mutual Exclusion
* 한 프로세스가 critical section 안에서 공유된 자원에 접근할 때 다른 프로세스는 이 공유된 자원에 접근하는 critical section에 접근하지 말아야 하는 요구사항

# Mutex Locks
* mutex = mutual exculsion
* critical section 문제를 해결하기 위해 사용하는 tool
* acquire(): lock을 요구한다.
* release(): lock을 풀어준다.
* lock을 기다리는 프로세스는 계속해서 loop를 돌아야한다.
* mutex lock => spinlock
# Semaphores
* 프로세스 사이에서 신호를 전달하기 위해 사용하는 integer 값이다.
* initialize, decrement, increment 세 가지 연산은 수행하며 각 연산은 atomic하게 실행된다.
* decrement 연산은 프로세스를 blocking하는 것이며
* increment 연산은 프로세스를 unblocking하는 것이다.

# Monitors
* semaphore와 같은 기능을 가지나 semaphore보다 control이 쉽다.
* local data는 오직 모니터의 procedure로 접근가능하다.
* 프로세스는 monitor의 procedure 중 하나를 호출하면서 monitor에 들어간다.
* 한번에 하나의 프로세스만 하나의 monitor에서 실행할 수 있으며 다른 프로세스는 monitor를 호출하는 것이 blocked되며 사용 가능해질때까지 기다려야 한다.
