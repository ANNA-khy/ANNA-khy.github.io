# Paging
* 메인 메모리를 작은 고정된 크기인 frame으로 나눈다.
* Program은 컴파일러나 메모리 관리 시스템에 의해 여러 개의 page들로 나누어진다.
* frame안에 Internal fragmentation이 발생할 수 있다.
* External fragmentation은 발생하지 않는다.
* OS는 각 프로세스에 대해 각 page가 차지하는 frame들을 보여주는 page table을 유지해야 한다.
* OS는 free-frame 리스트를 유지해야 한다.
* 프로세서는 absolute address를 계산하기 위해 page number, offset을 사용한다.
> Simple Paging
> * 프로세스의 모든 page들은 메인 메모리 안에 있어야 한다.

> Virtual Memory Paging
> * 프로세스의 모든 page가 메인 메모리 frame 안에 있을 필요는 없다.
> * 메인 메모리로 page를 읽어들이기 위해서 page를 디스크로 내보내는 동작이 필요하다.


# Segmentation
* 각 프로세스는 여러 개의 segment들로 나누어지며 이 segment들이 로드됨으로써 프로세스가 로드되는 것이다.
* Internal fragmentation이 없다.
* External fragmentation이 생긴다.
* OS는 각 프로세스를 위해 load address와 각 segment의 길이에 대한 정보를 담고있는 segment table을 유지해야 한다.
* OS는 메인 메모리의 free hole 리스트를 유지해야 한다.
* 프로세서는 absolute address를 계산하기 위해 segment number, offset을 사용한다.
> Simple Segmentation
> * 프로세스의 모든 segment들이 메인 메모리 안에 있다.

> Virtual Memory Segmentation
> * 프로세스의 모든 segment들이 메인 메모리 안에 있을 필요는 없다.
> * 메인 메모리로 segment를 읽어들이기 위해서 segment를 디스크로 내보내는 동작이 필요하다.
