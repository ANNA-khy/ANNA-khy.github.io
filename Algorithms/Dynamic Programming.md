# Dynamic Programming
* Bottom-up 방식
* 문제의 입력사례에 대해서 해답을 계산하는 재귀 관계식을 세운다. -> 가장 작은 입력사례부터 먼저 해결하고 bottom-up 방식으로 전체 입력사례에 대한 답을 구한다.

# Traveling Sales-man Problem
* 여러 개의 방문해야 할 도시들이 있을 때 모두 도시를 방문하고 다시 출발한 도시로 돌아올 때 가장 짧은 route를 찾는 문제

# Floyd Algorithm
* 가중치(weight)를 가지고 있는 그래프에서 각 노드에서 다른 모든 노드로 가는 최단 경로를 구하는 문제에 대한 알고리즘
* 최단 경로 배열을 초기화(연결되어 있으면 두 노드 사이의 가중치로 초기화/연결되어 있지 않으면 무한으로 초기화)
* SP[i][j] = mininum(SP[i][j], SP[i][k]+SP[k][j])
