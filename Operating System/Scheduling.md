# Scheduling Policies

## FCFS(First Come First Served)
* 현재 실행중인 프로세스가 중단되면 ready queue에 있는 프로세스들 중 ready queue에 가장 오래 있는 프로세스가 실행을 위해 선택된다.
* FCFS는 service time이 긴 프로세스가 짧은 프로세스보다 먼저 도착하면 짧은 프로세스는 긴 프로세스가 종료될 때까지 기다려야 한다.
* I/O-bound 프로세스가 processor-bound 프로세서가 실행되고 있는 동안 ready queue에서 대기하고 있으면 I/O가 idle 상태가 된다.

## Round Robin
* 현재 프로세스가 실행 중일때 clock interrupt가 발생하면 실행 중인 프로세스는 ready queue로 가고 FCFS에 따라 다음 프로세스가 실행된다.
* 프로세서를 선점하기 전 time slicing으로 실행된 시간이 주어지며 이 시간의 길이는 주요한 설계 이슈이다.

## SPN(Shortest Process Next)
* 가장 짧은 프로세스를 먼저 실행시키는 방법이다.
* service time이 긴 프로세스는 starvation될 수도 있다.
* 각 프로세스가 요구하는 실행시간을 미리 알아야 하는데 미리 알기가 어렵다.
* exponential averaging: S<sub>n+1</sub> = 1/n T<sub>n</sub>+(n-1)/n S<sub>n</sub>

## SRT(Shortest Remaing Time)
* 남아있는 실행시간이 가장 짧을 것으로 예상되는 프로세스를 선택한다.
* SPN과 마찬가지로 남아있는 실행시간이 긴 프로세스는 starvation이 발생할 수 있다.

## HRRN(Highest Response Ratio Next)
* reponse ratio가 높은 프로세스를 선택한다.
* response ratio = (time spent waiting for the processor + expected service time)/(expected service time)
* 프로세서를 기다린 시간을 고려하여 starvation을 방지한다.

## Feedback
* 기본적으로 일정한 시간만큼 preemptive하게 스케쥴링하며 dynamic priority 메커니즘이 사용된다.
* 처음에 프로세스가 시스템에 들어올 때는 PQ0 queue(가장 우선순위가 높은 큐)에 들어오고 time quantum이 끝나면 다음 우선순위 큐에 들어가고 그 다음 실행 뒤에 다시 더 우선순위가 낮은 큐에 들어간다.
* 짧은 프로세스는 우선 순위가 낮은 큐에 들어가지 않고 금방 끝나며 service time이 긴 프로세스는 점점 우선순위가 낮아지게 된다.
* Round Robin과 함께 유닉스에서 사용되는 방식이다.
