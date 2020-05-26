# Linked-list

+ [Sort List](#sort-list)
+ [Intersection of Two Linked Lists](#intersection-of-two-linked-lists)
+ [Reorder List](#reorder-list)
+ [Linked List Cycle](#linked-list-cycle)
+ [Linked List Cycle II](#linked-list-cycle-ii)
+ [Remove Nth Node From End of List](#remove-nth-node-from-end-of-list)
+ [Merge Two Sorted Lists](#merge-two-sorted-list)
+ [Palindrome Linked List](#palindrome-linked-list)
+ [Middle of the Linked List](#middle-of-the-linked-list)
+ [Reverse Linked List](#reverse-linked-list)

## Sort List

https://leetcode.com/problems/sort-list/

```python
print('Hello world!')
```

## Intersection of Two Linked Lists

https://leetcode.com/problems/intersection-of-two-linked-lists/

```python
print('Hello world!')
```

## Reorder List

https://leetcode.com/problems/reorder-list/

```python
print('Hello world!')
```

## Linked List Cycle

https://leetcode.com/problems/linked-list-cycle/

```python
print('Hello world!')
```

## Linked List Cycle II

https://leetcode.com/problems/linked-list-cycle-ii/

```python
print('Hello world!')
```

## Remove Nth Node From End of List

https://leetcode.com/problems/remove-nth-node-from-end-of-list/

```python
print('Hello world!')
```

## Merge Two Sorted Lists

https://leetcode.com/problems/merge-two-sorted-lists/

```python
def mergeTwoLists(self, l1: ListNode, l2: ListNode) -> ListNode:
    head = ListNode(0)
    current = head
    while l1 and l2:
        if l1.val < l2.val:
            current.next = l1
            l1 = l1.next
        else:
            current.next = l2
            l2 = l2.next
        current = current.next
    if not l1:
        current.next = l2
    elif not l2:
        current.next = l1
    return head.next
```

## Palindrome Linked List

https://leetcode.com/problems/palindrome-linked-list/

```python
print('Hello world!')
```

## Middle of the Linked List

https://leetcode.com/problems/middle-of-the-linked-list/

```python
print('Hello world!')
```

## Reverse Linked List

https://leetcode.com/problems/reverse-linked-list/

```python
print('Hello world!')
```
