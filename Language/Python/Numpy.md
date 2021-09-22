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
## np.dot(a,b) vs np.matmul vs np.multiply vs a * b 
* np.dot과 np.matmul은 2차원에서는 일반적인 행렬의 곱
* a*b와 np.multiply는 array 단위의 곱
* 아래 코드에서 a, b는 a*b이 불가능하다.
~~~
import numpy as np
a = np.array([[1, 2, 3], [4,5,6]])
b = np.array([[1,2],[3,4],[5,6]])
c = np.array([1,2,3])

print(a.dot(b)) 
print(np.dot(a,b))
#[[22 28]
# [49 64]]
#[[22 28]
# [49 64]]
print(a*c)
#[[ 1  4  9]
# [ 4 10 18]]
print(b*b)
#[[ 1  4]
# [ 9 16]
# [25 36]]
~~~
## Broadcasting
