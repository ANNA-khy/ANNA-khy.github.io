# Queue
* FIFO(First In First Out) 구조
* enqueue(): 맨 뒤에 element를 삽입
* dequeue(): 맨 앞에 있는 element를 삭제
* peek(): 맨 앞에 있는 element를 return
* c++ 라이브러리 queue 사용
* c++ queue 구현
~~~
#include <iostream>
struct Node
{
public:
    int data;
    Node* next;
};
class Queue
{
private:
    Node* front;
    Node* rear;
    int size = 0;
public:
    Queue() : front(nullptr), rear(nullptr) {}
    void enqueue(int a) {
        Node* newnode = new Node;
        newnode->data = a;
        newnode->next = nullptr;

        if (front == nullptr) {
            front = newnode;
        }

        if (rear == nullptr) {
            rear = newnode;
        }
        else {
            rear->next = newnode;
            rear = newnode;
        }

        size++;
    }
    int dequeue() {
        int val = front->data;
        front = front->next;
        if (front == rear)
            rear = nullptr;
        size--;
        return val;
    }
    void PrintNode() {
        Node* it = front;
        while (it != nullptr) {
            std::cout << it->data;
            it = it->next;
        }
        std::cout << std::endl;
    }
    int peek() {
        return front->data;
    }
};
~~~
# Deque
* Double-ended queue
* front와 rear에서 모두 삽입/삭제가 가능
