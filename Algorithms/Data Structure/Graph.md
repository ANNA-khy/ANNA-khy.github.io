# Graph
* 연결되어 있는 객체를 표현하는 자료구조
* ex) 각 도시와 도시들 간의 거리를 표현하는 지도
* vertex(도시), edge(연결된 길)로 표현 => G = (V, E)
* undirected graph: 무방향 그래프 -> 간선이 양방향
* directed graph: 방향 그래프 -> 간선이 단방향
* weighted graph: 간선에 가중치가 할당된 그래프
* adjacent vertex: 간선으로 직접 연결된 vertex
* degree: 하나의 vertex에 인접한 vertex의 개수
* in-degree: edge의 방향이 vertex로 들어오는 edge의 개수
* out-degree: edge의 방향이 vertex에서 나가는 edge의 개수
* simple path: 시작 vertex와 마지막 vertex를 제외하고 중복되는 vertex가 없는 경로
* cycle: simple path에서 시작 vertex 마지막 vertex가 동일하다면 cycle
* connected graph: 모든 vertex는 모든 다른 vertex로 경로가 존재
* complete graph: 모든 vertex가 서로 연결
* adjacency matrix와 adjacency list로 표현

# Graph 구현(C++)
~~~
#include <iostream>
#include <vector>
#define MAX_SIZE 50
struct Node
{
public:
    int data;
    Node* link;
};
class Graph
{
private:
    std::vector<Node*> graph_list;

public:
    Graph() {}
    void insertNode(int a) {
        Node* newnode = new Node;
        newnode->data = a;
        newnode->link = nullptr;
        
        graph_list.emplace_back(newnode);
    }
    void insertEdge(int a, int b) {
        for (int i = 0; i < graph_list.size(); i++) {
            if (graph_list[i]->data == a) {
                Node* newedge = new Node;
                newedge->data = b;
                newedge->link = nullptr;
                Node* pre = graph_list[i];
                Node* it = graph_list[i]->link;
                while (it != nullptr) {
                    pre = it;
                    it = it->link;
                }
                pre->link = newedge;
                //insertEdge(b, a);
                return;
            }
        }
    }
    void deleteNode(int a) {
        for (int i = 0; i < graph_list.size(); i++) {
            if (graph_list[i]->data == a) {
                auto it = graph_list[i]->link;
                auto pre = graph_list[i];
                while (it != nullptr) {
                    delete pre;
                    pre = it;
                    it = it->link;
                }
            }
            else {
                auto it = graph_list[i]->link;
                auto pre = graph_list[i];
                while (it != nullptr) {
                    if (it->data == a) {
                        pre->link = it->link;
                        delete it;
                        it = pre->link;
                    }
                    else {
                        pre = it;
                        it = it->link;
                    }
                }
            } 
        }
    }
    void deleteEdge(int a, int b) {
        for (int i = 0; i < graph_list.size(); i++) {
            if (graph_list[i]->data == a) {
                auto it = graph_list[i]->link;
                auto pre = graph_list[i];
                while (it != nullptr) {
                    if (it->data == b) {
                        pre->link = it->link;
                        delete it;
                        return;
                    }
                    pre = it;
                    it = it->link;
                }
            }
        }
    }
};
~~~
