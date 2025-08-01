# Leetcode-226.-Invert-Binary-Tree
# Description
Given the root of a binary tree, invert the tree, and return its root.
# Solution
We can invert a binary tree by swapping the element of left and right nodes of a tree.

<img width="753" height="266" alt="image" src="https://github.com/user-attachments/assets/5d983b8b-c983-446c-a554-bd76755840b7" />
The base case is if there is no root , then return None.

# Algorithm
1. If the root is None , return None.
2. Else swap the positions of root's left element with root's right and root's right element with root's left.
3. Keep on doing this recursively.
4. Return the root
# Code
class Solution:

    def invertTree(self, root: Optional[TreeNode]) -> Optional[TreeNode]:
        if root is None:
            return None
        root.left,root.right=self.invertTree(root.right),self.invertTree(root.left)
        return root
# Time Complexity
Each node in the binary tree is visited exactly once.

At each node, only constant-time swapping operation is performed.

Time Complexity: O(n)
Where n is the total number of nodes in the tree.
