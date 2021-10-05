# Tree
* Hierarchical structure
* root: 하나의 tree 안에서 가장 높은 degree에 있는 노드
* subtree: tree에서 root 제외한 모든 노드
* edge: root와 subtree를 연결하는 선
* degree: 노드가 가지고 있는 child node의 개수
# BST(Binary Search Tree)
* 각 Node의 왼쪽 subtree에 있는 모든 Node들의 Key 값은 해당 Node의 Key 값보다 작거나 같고, 각 Node의 오른쪽 subtree에 있는 모든 Node들의 Key 값은 해당 Node의 Key 값보다 크거나 같다. -> Invariant
* search -> O(h) : h는 tree의 높이
* h가 n이 되면 O(h) = O(n)
~~~
#include <iostream>
struct Node
{
public:
    int data;
    Node* left;
    Node* right;
};
class Tree
{
private:
    Node* root;

    int size = 0;
public:
    Tree() : root(nullptr) {}
    void insertNode(int a) {
        Node* newnode = new Node;
        newnode->data = a;
        newnode->left = nullptr;
        newnode->right = nullptr;

        Node* it = root;
        Node* pre = it;
        if (it == nullptr) {
            root = newnode;
            size++;
            return;
        }
        while (it != nullptr) {
            if (it->data >= a&&it->left!=nullptr)
                it = it->left;
            else if (it->data<a&&it->right!=nullptr)
                it = it->right;
            else if (it->data >= a && it->left == nullptr) {
                it->left = newnode;
                break;
            }
            else {
                it->right = newnode;
                break;
            }
        }
        
        size++;
    }
    void deleteNode(int a) {
        Node* it = root;
        Node* pre = root;

        while (it->data != a) {
            if (it->data > a) {
                pre = it;
                it = it->left;
            }
            else if (it->data < a) {
                pre = it;
                it = it->right;
            }
            else {
                if (it->left == nullptr) {
                    if (pre->left && pre->left->data == a)
                        pre->left = it->right;
                    else
                        pre->right = it->right;
                        
                }
                else if (it->right == nullptr) {
                    if (pre->left && pre->left->data == a)
                        pre->left = it->left;
                    else
                        pre->right = it->left;
                }
                else {

                }
                delete it;
                return;
            }
        }
        size--;
    }
    void printDFS() { // inorder
        DFS(root);
        std::cout << std::endl;
    }
    void printBFS() {
        if (root) {
            std::cout << root->data << " ";
            BFS(root);
        }
        std::cout << std::endl;
    }
private:
    void DFS(Node* it) {
        if (it) {
            DFS(it->left);
            std::cout << it->data << " ";
            DFS(it->right);
        }
    }
    void BFS(Node* it) {
        if (it->left)
            std::cout << it->left->data << " ";
        if (it->right)
            std::cout << it->right->data << " ";
        if (it->left)
            BFS(it->left);
        if (it->right)
            BFS(it->right);
    }
};
~~~
