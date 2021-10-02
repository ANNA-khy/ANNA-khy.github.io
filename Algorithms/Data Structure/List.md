> # List
* 원하는 위치에 원소를 삽입할 수 있고 삭제할 수 있다.
## Array list
* 구현이 간단하며 데이터에 접근하는 것은 빠르다.
* 크기가 고정적
* 삽입/삭제 시에 오버헤드 -> 한칸씩 이동해야 하므로
## Linked list
* 크기가 가변적
* 삽입/삭제 시에 데이터 이동이 없다.
* array list에 비해 데이터 간 연결을 위한 공간이 추가로 필요하며 구현이 복잡하다.
* C++ 구현
~~~
#include <iostream>
struct Node
{
public:
    int data;
    Node* next;
};
class LinkedList
{
private:
    Node* head;
    Node* tail;
    int size = 0;
public:
    LinkedList() : head(nullptr), tail(nullptr) {}
    void AddNode(int a) {
        Node* newnode = new Node;
        newnode->data = a;
        newnode->next = nullptr;

        if (head == nullptr) {
            head = newnode;
            tail = newnode;
        }
        else {
            tail->next = newnode;
            tail = newnode;
        }

        size++;
    }
    void RemoveNode(int a) {
        Node* it = head;
        Node* pre = head;
        while (it != nullptr) {
            if (it->data != a) {
                pre = it;
                it = it->next;
                continue;
            }
            if (it == head) {
                head = it->next;
            }
            else if (it == tail) {
                pre = tail;
                tail->next = nullptr;
            }
            else {
                pre->next = it->next;
            }
            delete it;
            size--;
            break;
        }
    }
    void PrintNode() {
        Node* it = head;
        while (it != nullptr) {
            std::cout << it->data;
            it = it->next;
        }
        std::cout << std::endl;
    }

};
~~~
