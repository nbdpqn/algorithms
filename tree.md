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
print('Hello world!')
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
print('Hello world!')
```

## Subtree of Another Tree

https://leetcode.com/problems/subtree-of-another-tree/

```python
print('Hello world!')
```

## Binary Tree Level Order Traversal

https://leetcode.com/problems/binary-tree-level-order-traversal/

```python
print('Hello world!')
```

## Path Sum

https://leetcode.com/problems/path-sum/

```python
print('Hello world!')
```

## Invert Binary Tree

https://leetcode.com/problems/invert-binary-tree/

```python
print('Hello world!')
```

## Same Tree

https://leetcode.com/problems/same-tree/

```python
print('Hello world!')
```

## Maximum Depth of Binary Tree

https://leetcode.com/problems/maximum-depth-of-binary-tree/

```python
print('Hello world!')
```

## Symmetric Tree

https://leetcode.com/problems/symmetric-tree/

```python
print('Hello world!')
```

## Binary Tree Inorder Traversal

https://leetcode.com/problems/binary-tree-inorder-traversal/

```python
print('Hello world!')
```
