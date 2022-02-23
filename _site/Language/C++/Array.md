# std::arrary
* 고정 길이 배열
* array<type, size> 변수명;
* 원소에 접근하기 위해서는 [], at 사용 가능하며 at은 범위 검사를 하기 때문에 더 느리다.(범위를 벗어나면 out_of_range 예외 발생)
# std::vector
* 가변 길이 배열
* vector<type> 변수명;
* 원소에 접근하기 위해서는 [], at 사용 가능하며 at은 범위 검사를 하기 때문에 더 느리다.(범위를 벗어나면 out_of_range 예외 발생)
* 검색(find)/삽입(insert)/삭제(erase) 연산 -> O(n) => 시간복잡도 주의!
* 앞뒤 삽입/삭제 -> O(1)
* 연속된 메모리에 저장됨 -> 확장이 필요할 시 전체 vector를 재할당 해야함
* push_back/emplace_back은 모두 vector의 끝에 element를 추가하는 함수로 push_back은 임시 객체를 생성/파괴하는 과정이 있지만 emplace_back은 그러한 과정이 없다. -> emplace_back은 vector 내에 직접 객체 추가 => emplace_back이 성능에 있어서 더 효율적
