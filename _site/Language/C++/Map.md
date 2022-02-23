# Map(map)
* 연관 컨테이너
* (key, value)
* key는 순서가 있는 모든 타입이 될 수 있다.
* key 중복은 허용되지 않는다.
* key를 찾을 수 없다면 value를 디폴트 값으로 하는 새로운 항목을 삽입하고 이 값을 가리키는 레퍼런스를 return
* 각 데이터에 접근하기 위한 시간 복잡도: O(log n) -> 검색/삽입/삭제
  
# Hash table(unordered_map)
* 연관 컨테이너
* (key, value)
* unordered_map은 해시 테이블로 구현
* 해시 충돌이 많이 일어나면 성능이 떨어진다.
* 각 데이터에 접근하기 위한 시간 복잡도: O(1) -> 검색/삽입/삭제
* bucket: 키 값이 key인 요소의 bucket number를 return
* count: key와 매핑된 값들의 개수

# Set(set)
* 연관 컨테이너
* (key)
* 정렬되어 있으며 중복은 허용하지 않는다. -> binary search tree 구조
* 각 데이터에 접근하기 위한 시간 복잡도: O(log n) -> 검색/삽입/삭제
