Weekly Coding #5: Skyrail Station Navigator
Summary

This program works with binary trees and binary search trees (BST). It performs tree traversals (preorder, inorder, and postorder) to visit nodes in different orders. It also implements BST operations such as searching for a value and inserting a new value. These functions help organize and efficiently access data in a tree structure.

Approach
Preorder traversal: Visit the current node first, then recursively visit the left subtree, then the right subtree.
Inorder traversal: Recursively visit the left subtree, then the current node, then the right subtree.
Postorder traversal: Recursively visit the left subtree, then the right subtree, then the current node.
BST search: Compare the target value with the current node. If smaller, go left; if larger, go right; if equal, return True.
BST insert: Recursively find the correct position based on value comparison. Insert a new node if the spot is empty and ignore duplicates.
Complexity
preorder_values
Time: O(n)
Space: O(h)
Why: Visits every node once; recursion stack depends on tree height.
inorder_values
Time: O(n)
Space: O(h)
Why: Traverses all nodes once; recursion depth depends on height.
postorder_values
Time: O(n)
Space: O(h)
Why: Each node is processed once; recursion stack uses height.
bst_contains
Time: O(h)
Space: O(h)
Why: Only one path is followed from root to leaf based on comparisons.
bst_insert
Time: O(h)
Space: O(h)
Why: Traverses one path to insert; recursion stack depends on height.
Edge-Case Checklist
 Empty tree traversal returns []
→ Functions return an empty list when root is None.
 Single-node traversal works correctly
→ Returns a list with just that node’s value.
 bst_contains returns False for an empty tree
→ Immediately returns False if root is None.
 bst_contains returns False when the target is missing
→ Recursion reaches a None node and returns False.
 bst_insert creates a root when the tree is empty
→ If root is None, a new node is created.
 bst_insert ignores duplicate values
→ If value equals current node, nothing is inserted.
 I tested at least one deeper insert case
→ Verified inserting values like 55 or 25 goes to correct position.
Assistance & Sources
AI used? (Y/N): Y
What AI helped with: Understanding traversal logic, recursion, and verifying implementation correctness.
Other sources used: Class notes and lecture materials.