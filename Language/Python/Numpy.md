# Numpy
* 과학 계산에 사용되는 라이브러리로 array의 빠른 연산을 지원한다.
## ndarray
* 같은 종류의 data type만을 담을 수 있다.
* 크기는 생성할 때 고정된 크기로 정해지면 size를 바꾸는 것은 기존의 array를 삭제하고 새로운 array를 생성하는 것이다.
* 큰 숫자의 연산도 파이썬의 built-in sequence 보다 빠르게 수행하며 간결하다.
* for loop를 이용한 배열 곱 연산을 다음과 같이 간단하게 나타낸다.
~~~ 
c = a * b
~~~
## np.dot(a,b)
* 1차원에서는 inner product, 2차원에서는 행렬의 곱(matmul을 쓰자!) 
* a는 N차원 b는 1차원이면 sum product
* a는 N차원 b는 M차원(M>=2)이면 sum product
~~~
import numpy as np

a = np.array([[1, 2, 3], [4,5,6]])
b = np.array([[1,2],[3,4],[5,6]])

print(np.dot(a,b))
# [[22 28]
# [49 64]]
~~~
## np.inner(a,b)
* 1차원에서는 inner product, 더 높은 차원에서는 마지막 축에 대한 sum product
* a와 b의 shape에서 마지막 차원은 일치해야 한다. 
~~~
import numpy as np

a = np.array([[1, 2, 3], [4,5,6]])
c = np.array([1,2,3])

print(np.inner(a,c))
# [14, 32]
~~~
## np.matmul(a, b)
* matrix product
* shape는 (n, k)(k, m) => (n, m)
~~~
import numpy as np

a = np.array([[1, 2, 3], [4,5,6]])
b = np.array([[1,2],[3,4],[5,6]])
c = np.array([1,2,3])

print(np.matmul(a,b))
# [[22 28]
# [49 64]]
print(np.matmul(a,c))
# [14 32]
~~~
## np.tensordot(a, b)
* 특정한 축에 대한 tensor dot product
~~~
import numpy as np

a = np.array([[1, 2, 3], [4,5,6]])
b = np.array([[1,2],[3,4],[5,6]])

print(np.tensordot(a,b,axes=([0,1],[1,0])))
# 86
~~~
## np.multiply(a, b) = a*b
* a, b를 곱하며 a와 b의 shape가 같지 않다면 broadcast한다.
~~~
import numpy as np

a = np.array([[1, 2, 3], [4,5,6]])
b = np.array([[1, 2, 3], [4,5,6]])
c = np.array([1,2,3])

print(np.multiply(a, b))
# [[ 1  4  9]
# [16 25 36]]
print(np.multiply(a,c))
# [[ 1  4  9]
# [ 4 10 18]]
~~~
## Broadcasting
