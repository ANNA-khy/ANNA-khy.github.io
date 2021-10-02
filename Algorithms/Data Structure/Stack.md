# Stack
* LIFO(List In First Out) 구조
* push(): 삽입
* pop(): 삭제
* 함수 호출 시 함수 복귀 주소를 기억할 때 stack을 사용
* c++ stack 라이브러리
* c++ 구현
~~~
#include <iostream>
struct Node
{
public:
    int data;
    Node* next;
};
class Stack
{
private:
    Node* top;
    int size = 0;
public:
    Stack() : top(nullptr) {}
    void push(int a) {
        Node* newnode = new Node;
        newnode->data = a;
        newnode->next = top;
        top = newnode;

        size++;
    }
    int pop() {
        int val = top->data;
        top = top->next;
        return val;
    }
    void PrintNode() {
        Node* it = top;
        while (it != nullptr) {
            std::cout << it->data;
            it = it->next;
        }
        std::cout << std::endl;
    }
};
~~~
