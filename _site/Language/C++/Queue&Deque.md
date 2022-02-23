# Queue (#include &#60;queue&#62;)
* Queue는 FIFO(First In First Out) 구조
* 앞에서만 삭제가능 뒤에서만 삽입가능
* 삽입 -> push(data) 
* 삭제 -> pop() => 맨 앞의 원소를 pop
* front(), back() => 각각 맨 앞, 맨 뒤 원소를 return

# Priority Queue(Heap) (#include &#60;queue&#62;)
* 우선순위가 있는 queue로 가장 우선 순위가 큰 수부터 제거된다.
* 오름차순으로 하기 위해서는 greater를 사용한다.
* 삽입 -> push(data) => 우선 순위에 따라 적절한 위치에 삽입한다.
* 삭제 -> pop() => 우선 순위가 가장 큰 원소를 pop
* top(), back() => 우선 순위가 가장 높은 원소, 가장 낮은 원소를 return

# Deque (#include &#60;queue&#62;)
* Double Ended Queue
* 앞 뒤 모두 삽입, 삭제 가능 => push_front(data), pop_front(), push_back(data), pop_front()
* capacity()가 없다.
* index를 이용해 각 원소들에 접근할 수 있다.
* 연속되지 않은 메모리에 저장된다.
