# Queue (#include &#60;queue&#62;)
* Queue는 FIFO(First In First Out) 구조
* 앞에서만 삭제가능 뒤에서만 삽입가능
* 삽입 -> push(data) 
* 삭제 -> pop() => 맨 앞의 원소를 pop
* front(), back() => 각각 맨 앞, 맨 뒤 원소를 return

# Deque (#include &#60;queue&#62;)
* Double Ended Queue
* 앞 뒤 모두 삽입, 삭제 가능 => push_front(data), pop_front(), push_back(data), pop_front()
* capacity()가 없다.
* index를 이용해 각 원소들에 접근할 수 있다.
* 연속되지 않은 메모리에 저장된다.
