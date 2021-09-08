# Greedy Algorithm
* 현재 가장 좋은 답을 고르는 알고리즘(미래는 고려하지 않는다.) -> local optimam => 항상 (globally) 최적의 해답을 얻는다는 보장은 없다.
* Selection procedure: 집합(해답)에 추가할 원소를 greedy 알고리즘에 따라 선택한다.
* Feasibility check: 새로 원소를 추가한 집합이 해답에 적절한지 검사한다.
* Solution check: 새로 원소를 추가한 집합이 해답이 될 수 있는지 확인한다. => 해답이 될 수 없다면 반복
* 장점
  * 쉽고 구현하기 간단
  * Test Bed
  * local optima

# Minimum Spanning Tree
* spanning tree: 그래프의 모든 마디를 포함하면서 tree인 연결된 그래프 -> simple cycle이 없다.
* 가중치의 합이 최소값인 spanning tree를 구하는 문제
* Prim's Algorithm
  * 시작 노드를 선택 </br>→ 가장 가까이 있는 마디를 선택 </br>→ 모든 노드를 포함할 때까지 현재 그래프에서 가장 가까이 있는 마디를 선택하는 것을 반복
  * 시간복잡도: n^2
* Kruskal's Algorithm
  * edge를 가중치가 작은 순으로 정렬 </br>→ 가장 작은 edge를 선택 </br>→ feasiblity check를 해가면서 해답이 될 때까지 반복
  * 시간복잡도: n^2 * logn
# Dijkstra Algorithm
* 각 노드에서 다른 모든 노드로의 최단 경로를 구하는 Floyd 알고리즘과 달리 한 노드에서 다른 모든 노드로 가는 최단 경로를 계산하는 알고리즘
* 다른 노드로 최단 경로를 구하려고 하는 노드(v1)를 원소로 하는 집합 Y를 초기화하고 edge의 집합 F도 공집합으로 초기화 </br>→ Y에 있는 노드만 거쳐서 가는 경로 중 최단경로인 노드를 V(전체 노드 집합)-Y에서 선택 </br>→ 새로 선택한 노드를 Y에 추가하고 edge도 F에 추가</br> → Y==V일때까지 반복
* 시간복잡도: n^2

참고: 알고리즘 기초(Richard E. Neapolitan)
