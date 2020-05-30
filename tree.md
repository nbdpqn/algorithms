# Tree

+ [Binary Search Tree Iterator](#binary-search-tree-iterator)
+ [Validate Binary Search Tree](#validate-binary-search-tree)
+ [Kth Smallest Element in a BST](#kth-smallest-element-in-a-bst)
+ [Subtree of Another Tree](#subtree-of-another-tree)
+ [Binary Tree Level Order Traversal](#binary-tree-level-order-traversal)
+ [Path Sum](#path-sum)
+ [Invert Binary Tree](#invert-binary-tree)
+ [Same Tree](#same-tree)
+ [Maximum Depth of Binary Tree](#maximum-depth-of-binary-tree)
+ [Symmetric Tree](#symmetric-tree)
+ [Binary Tree Inorder Traversal](#binary-tree-inorder-traversal)

## Binary Search Tree Iterator

https://leetcode.com/problems/binary-search-tree-iterator/

```python
class BSTIterator:
    def __init__(self, root: TreeNode):
        self.stack = list()
        self.addLeft(root)

    def addLeft(self, root):
        while root:
            self.stack.append(root)
            root = root.left

    def next(self) -> int:
        top = self.stack.pop()
        if top.right:
            self.addLeft(top.right)
        return top.val

    def hasNext(self) -> bool:
        return len(self.stack) > 0
```

## Validate Binary Search Tree

https://leetcode.com/problems/validate-binary-search-tree/

```python
def isValidBST(self, root: TreeNode) -> bool:
    if not root:
        return True
    stack = [(root, float('-inf'), float('inf'))]
    while stack:
        root, lower, upper = stack.pop()
        if not root:
            continue
        value = root.val
        if value <= lower or value >= upper:
            return False
        stack.append((root.right, value, upper))
        stack.append((root.left, lower, value))
    return True
```

## Kth Smallest Element in a BST

https://leetcode.com/problems/kth-smallest-element-in-a-bst/

```python
def kthSmallest(self, root: TreeNode, k: int) -> int:
    assert k > 0
    stack = list()
    while True:
        while root:
            stack.append(root)
            root = root.left
        assert stack # stack is empty if and only if k > size of tree
        root = stack.pop()
        k -= 1
        if k == 0:
            return root.val
        root = root.right
```

## Subtree of Another Tree

https://leetcode.com/problems/subtree-of-another-tree/

```python
def isEqual(self, s: TreeNode, t: TreeNode) -> bool:
    if not s and not t:
        return True
    if not s or not t:
        return False
    return s.val == t.val and self.isEqual(s.left, t.left) and self.isEqual(s.right, t.right)


def isSubtree(self, s: TreeNode, t: TreeNode) -> bool:
    return s and (self.isEqual(s, t) or self.isSubtree(s.left, t) or self.isSubtree(s.right, t))
```

## Binary Tree Level Order Traversal

https://leetcode.com/problems/binary-tree-level-order-traversal/

```python
def levelOrder(self, root: TreeNode) -> List[List[int]]:
    if not root:
        return list()
    result = list()
    currentLevel = [root]
    while currentLevel:
        queue = currentLevel
        currentLevel = []
        result.append([elem.val for elem in queue])
        while queue:
            node = queue.pop(0)
            if not node.left:
                currentLevel.append(node.left)
            if not node.right:
                currentLevel.append(node.right)
    return result
```

## Path Sum

https://leetcode.com/problems/path-sum/

```python
def hasPathSum(self, root: TreeNode, sum: int) -> bool:
    if not root:
        return False
    elif not root.left and not root.right and sum - root.val == 0:
        return True
    elif not root.left and not root.right and sum - root.val != 0:
        return False
    else:
        return self.hasPathSum(root.right, sum - root.val) or self.hasPathSum(root.left, sum - root.val)
```

## Invert Binary Tree

https://leetcode.com/problems/invert-binary-tree/

```python
def invertTree(self, root: TreeNode) -> TreeNode:
    if not root:
        return None
    right = self.invertTree(root.right)
    left = self.invertTree(root.left)
    root.left = right
    root.right = left
    return root
```

## Same Tree

https://leetcode.com/problems/same-tree/

```python
def isSameTree(self, p: TreeNode, q: TreeNode) -> bool:
    if not p and not q:
        return True
    elif not p or not q:
        return False
    elif p.val != q.val:
        return False
    else:
        return self.isSameTree(p.left, q.left) and self.isSameTree(p.right, q.right)
```

## Maximum Depth of Binary Tree

https://leetcode.com/problems/maximum-depth-of-binary-tree/

```python
def maxDepth(self, root: TreeNode) -> int:
    if not root:
        return 0
    else:
        return 1 + max(self.maxDepth(root.left), self.maxDepth(root.right))
```

## Symmetric Tree

https://leetcode.com/problems/symmetric-tree/

```python
def isMirrored(self, first: TreeNode, second: TreeNode) -> bool:
    if not first and not second:
        return True
    if not first or not second:
        return False
    return first.val == second.val and self.isMirrored(first.right, second.left) and \
           self.isMirrored(first.left, second.right)


def isSymmetric(self, root: TreeNode) -> bool:
    return self.isMirrored(root, root)
```

## Binary Tree Inorder Traversal

https://leetcode.com/problems/binary-tree-inorder-traversal/

```python
def inorderTraversal(self, root: TreeNode) -> List[int]:
    stack = list()
    result = list()
    current = root
    while not current or not stack:
        while current:
            stack.append(current)
            current = current.left
        current = stack.pop()
        result.append(current.val)
        current = current.right
    return result
```
