# Backtracking 개념
* DFS(Depth First Search)을 사용하는 알고리즘
* 집합에서 주어진 기준대로 원소의 순서를 선택하는 문제에 사용한다. 
* 이론적인 시간복잡도: O(n^n)


# State Space Tree
* 현재 문제를 해결하는 상태를 각각의 노드로 나타낸 트리

## Promising & Nonpromising
* Promising: nonpromising이 아닌 경우
* Nonpromising: 마디가 해답이 될 가능성이 없다.
* Pruning: 해당 노드가 nonpromising하면 더 이상 탐색을 하지 않는 것으로 nonpromising이라면 부모 노드로 backtraking한다.
* Pruned state space tree: 유망한 마디로만 구성된 state space tree(부분 트리)

## Bounding Function(Evaluation Function)
* f = g + h
* g -> 현재까지의 정확한 값(cost)
* h -> 미래에 얻을 수 있는 최대 이익(heuristic)

# Monte Carlo Algorithm
* 몬테칼로 알고리즘을 사용해서 backtracking의 효율성을 추정한다.
* 표본공간의 무작위 표본의 평균치를 가지고 표본공간에서 정의된 무작위변수의 기대치를 추정한다.(알고리즘 기초)

# 관련문제
* n-Queens Problem: 서로 공격할 수 없도록 n개의 queen을 n*n 크기를 가지는 체스판에 배치시키는 문제 => O(n^n) 이론적인 time complexity는 변함없음
* m-graphes 색칠하기
* Hamiltoninan Circuits Problem

참고: 알고리즘 기초(Richard E. Neapolitan)
