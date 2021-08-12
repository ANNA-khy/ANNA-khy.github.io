> # Heap
* 최대값(or 최소값)을 root로 하는 자료구조로 Node의 Key 값이 해당 Node의 children의 Key 값보다 크다(or 작다). => Heap Property
* Max_heapify -> 하나의 부분에서 heap property가 만족하지 못했을 때 이를 heap property를 만족하도록 만드는 것
* Build_Max_Heap -> O(n) => 빠르다
#
> # BST(Binary Search Tree)
* 각 Node의 왼쪽 subtree에 있는 모든 Node들의 Key 값은 해당 Node의 Key 값보다 작거나 같고, 각 Node의 오른쪽 subtree에 있는 모든 Node들의 Key 값은 해당 Node의 Key 값보다 크거나 같다. -> Invariant
* search -> O(h) : h는 tree의 높이
