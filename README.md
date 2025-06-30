# IIMS-Data Structures and Algorithms
Binary Search
 Let's take an example. A = [1, 3, 7, 8, 10, 11, 12, 15, 19, 21, 22, 23, 29, 31, 37]. 
This list can be seen as a binary tree (although there is no need to build the tree):

             15
        ____/  \____
       /            \
    __8__           _23__
   /     \         /     \
  3      11       21     31
 / \    /  \     /  \   /  \
1   7  10   12  19  22 29  37

A binary search for e = 27 (for example) will undergo the following steps

b0) Let T, R be the tree and its root respectively

                 15 (R)
            ____/  \____
           /            \
        __8__           _23__
       /     \         /     \
      3      11       21     31
     / \    /  \     /  \   /  \
    1   7  10   12  19  22 29  37
b1) Compare e to R: e > 15. Let T, R be T right subtree and its root respectively

                 15
            ____/  \____
           /            \
        __8__           _23_(R)
       /     \         /     \
      3      11       21     31
     / \    /  \     /  \   /  \
    1   7  10   12  19  22 29  37
b2) Compare e to R: e > 23. Let T, R be T right subtree and its root respectively

                 15
            ____/  \____
           /            \
        __8__           _23__
       /     \         /     \
      3      11       21     31 (R)
     / \    /  \     /  \   /  \
    1   7  10   12  19  22 29  37
b3) Compare e to R: e < 31. Let T, R be T left subtree and its root respectively

                 15
            ____/  \____
           /            \
        __8__           _23__
       /     \         /     \
      3      11       21     31___
     / \    /  \     /  \   /     \
    1   7  10   12  19  22 29 (R)  37
b4) Compare e to R: e <> 29: the element is not in the list, since T has no subtree.
