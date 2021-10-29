# Automata
* 계산 능력이 있는 기계가 입력 데이터를 계산하여 출력 데이터를 산출하는 과정을 시각화하여 모델로 나타낸 것
## Finite Automata
* temporary memory가 없다.
* 가장 power가 약한 automata이다.
### DFA(Deterministic Finite Automata)
* state의 집합, input alphabet, trasition 함수, 초기 state, final state의 집합으로 이루어져 있다.
* 항상 한 state에서 다른 state(혹은 자기자신)으로 transition이 존재한다.
### NFA(Nondeterministic Finite Automata)
* state의 집합, input alphabet, trasition 함수, 초기 state, final state의 집합으로 이루어져 있다.
* 한 state에서 다른 state로의 transition이 존재하지 않을 수도 있다.
* 모든 DFA는 NFA이다.
### Regular languages
### Regular grammars
## Pushdown Automata
* Context-free languages
* Context-free grammars
## Turing Machines
* halting: 만약에 가능한 transition이 존재하지 않는다면 그 기계는 중지(halt)한다.
### Halting Problem
* 프로그램 P에 입력(input)을 넣었을 때 프로그램 P가 답을 낼 수 있는지(halt) 혹은 답을 내지 못하고 무한 루프에 빠지는지 알 수 있는 프로그램 H가 존재하는가?
* H(P, input) => P가 멈추면 true / P가 무한루프에 빠지면 false
* E(P) => H(P, P)가 false이면 true / 그렇지 않으면 무한루프
* E(E)?
  * H(E, E)가 true이면 E는 halt하는 프로그램이지만 H(P, P)가 true라면 무한루프에 빠지게됨 => 모순
  * H(E, E)가 false이면 E는 무한루프에 빠지는 프로그램이지만 H(P, P)는 false 이므로 true를 반환하고 종료 => 모순
* 프로그램 P에 입력(input)을 넣었을 프로그램 P가 답을 낼 수 있는지(halt) 혹은 답을 내지 못하고 무한 루프에 빠지는지 알 수 있는 프로그램 H가 존재 => 위 프로그램으로 모순발생
* 프로그램 P에 입력(input)을 넣었을 때 프로그램 P가 답을 낼 수 있는지(halt) 혹은 답을 내지 못하고 무한 루프에 빠지는지 알 수 있는 프로그램 H가 존재하지 않는다.
