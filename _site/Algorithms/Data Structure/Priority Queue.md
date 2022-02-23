# Priority Queue
* 데이터에 우선 순위를 부여하고 우선순위가 가장 높은 데이터가 가장 빨리 나간다.
* heap는 priority queue의 구현방법 중 가장 효율적
# Heap
* 최대값(or 최소값)을 root로 하는 자료구조로 Node의 Key 값이 해당 Node의 children의 Key 값보다 크다(or 작다). => Heap Property
* Max_heapify -> 하나의 부분에서 heap property가 만족하지 못했을 때 이를 heap property를 만족하도록 만드는 것
* Build_Max_Heap -> O(n) => 빠르다
* 삽입/삭제 -> O(logn)
* max heap 구현
~~~
#include <iostream>
#include <vector>
template <typename T>
class Heap
{
private:
    std::vector<T> heap;
    
public:
    Heap() { heap.emplace_back(-1); }
    void insert(T a) {
        int cidx = heap.size();
        int pidx;
        heap.emplace_back(a);
        
        while (true) {
            pidx = cidx / 2;
            if (pidx!=0&&heap[pidx] < heap[cidx]) {
                int tmp = heap[cidx];
                heap[cidx] = heap[pidx];
                heap[pidx] = tmp;
                cidx = pidx;
            }
            else
                break;
        }
    }
    
    T pop() {
        int idx = 1;
        T big = heap[idx];
        heap[idx] = heap[heap.size()-1];
        heap.erase(heap.begin()+ heap.size()-1);

        
        while (idx*2 < heap.size()) {
            int maxc = (heap[idx * 2] > heap[idx * 2 + 1]) ? idx * 2 : idx * 2 + 1;
            if (heap[maxc] > heap[idx]) {
                int tmp = heap[idx];
                heap[idx] = heap[maxc];
                heap[maxc] = tmp;
                idx = maxc;
            }
            else
                break;
        }
        return big;
    }
};
~~~
