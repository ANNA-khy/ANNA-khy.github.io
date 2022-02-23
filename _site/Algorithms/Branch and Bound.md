# B&B 개념
* Backtracking을 개선한 알고리즘
* 트리 횡단 방법에 구애받지 않는다. -> 자식노드를 탐색하다가도 현재 노드보다 더 좋은 bound 값을 가지는 노드를 방문할 수 있다.
* 최적화 문제에서만 사용한다.
* 마디가 유망한지 bound 값으로 결정하고 자식 노드를 탐색할 때에도 bound 값이 가장 최적값에 가까운 노드를 방문한다.

# Promising & Nonpromising
* Promising: Bound 값이 현재 최적의 답과 같거나 더 좋다.
* Nonpromising: Bound 값이 현재 최적의 답보다 좋지 않다.

참고: 알고리즘 기초(Richard E. Neapolitan)
