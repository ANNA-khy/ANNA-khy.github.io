# Selection Sort
* 현재 인덱스의 element에서 뒤에 있는 element를 조회하면서 해당 순서에 와야할 element를 찾아서 현재 인덱스의 element와 swap한다.
* 시간복잡도: O(n^2)
# Insertion Sort
* 두번째 인덱스부터 시작하여 현재 인덱스보다 앞에 있는 element들을 뒤에서부터 검사하며 비교 값보다 element가 크다면 인덱스를 1 감소하여 검사한다.
* 비교 값보다 element가 작다면 해당 위치에 원소를 삽입한다.
* 시간복잡도: O(n^2)
# Bubble Sort
* 첫번째 인덱스부터 시작하여 현재 인덱스와 그 다음 인덱스의 element를 비교하여 큰 수를 뒤로 보내는 동작을 배열을 처음부터 끝까지 진행한다. -> 맨 뒤에는 가장 큰 원소
* 시간복잡도: O(n^2)
# Merge Sort
* Divide and Conquer 방식으로 sorthing을 하는 알고리즘으로 배열을 크기가 1일때까지 나눈뒤 다시 합친다.
* 이때 합칠 때 sorthing을 진행한다.
* 시간복잡도: O(nlogn) -> n을 divide => log n, divide된 배열을 sorthing => n

# Quick Sort
* pivot 값을 랜덤하게 혹은 중간값으로 정한다.
* pivot 값보다 작은 원소와 큰 원소를 pivot 값을 기준으로 정렬한다.
* 다시 나누어진 배열을 quick sort로 정렬한다.
* 시간복잡도: 평균 -> O(nlogn) 최악 -> O(n^2) => pivot 값을 최대값 or 최소값으로 선택한 경우

# Heap Sort
# Radix Sort

