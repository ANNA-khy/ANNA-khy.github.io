# Echelon Form
* 최소한 1개 이상의 entry가 0이 아닌 row는 모든 entry가 0인 row보다 위에 있다.
* nonzero row의 leading entry는 그 row보다 위에 있는 leading entry의 오른쪽에 있다.
* 한 column에서 leading entry보다 밑에 있는 모든 entry는 0이다.
* ex)
\begin{bmatrix}
1 & -2 & -3 & 1 \\\\
0 & 0 & -1/2 & -1 \\
0 & 0 & 1 & 2 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
\end{bmatrix}
# RREF(Reduced Row Echelon Form)
* 아래와 같은 조건을 만족하는 Echelon Form을 Reduced Row Echelon Form이라고 한다.
* 모든 leading entry는 1이다.
* 각 leading entry는 그 column에서 유일한 nonzero entry이다.
* ex)
\begin{bmatrix}
1 & 0 & 0 & -1 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 2 \\
\end{bmatrix}
## Pivot
* Pivot position: EF에서 leading entry의 위치
* Pivot: pivot position에서 0이 아닌 숫자로 row operation으로 0을 만들기 위해서 사용된다.
