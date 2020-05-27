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
def merge(self, left: ListNode, right: ListNode) -> ListNode:
    head = ListNode(0)
    current = head
    while left and right:
        if left.val <= right.val:
            current.next = left
            left = left.next
        else:
            current.next = right
            right = right.next
        current = current.next
    if not left:
        current.next = right
    elif not right:
        current.next = left
    return head.next


def sortList(self, head: ListNode) -> ListNode:
    if not head or not head.next:
        return head

    mid = head
    temp = head
    while mid.next and temp.next and temp.next.next:
        mid = mid.next
        temp = temp.next.next

    right = self.sortList(mid.next)
    mid.next = None
    left = self.sortList(head)
    return self.merge(left, right)
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
def removeNthFromEnd(self, head: ListNode, n: int) -> ListNode:
    start = ListNode(0)
    start.next = head
    
    first = start
    second = start
    for i in range(1, n + 2):
        first = first.next
    while first:
        first = first.next
        second = second.next
    second.next = second.next.next
    return start.next
```

## Merge Two Sorted Lists

https://leetcode.com/problems/merge-two-sorted-lists/

```python
print('Hello world!')
```

## Palindrome Linked List

https://leetcode.com/problems/palindrome-linked-list/

```python
print('Hello world!')
```

## Middle of the Linked List

https://leetcode.com/problems/middle-of-the-linked-list/

```python
def middleNode(self, head: ListNode) -> ListNode:
    first = head
    second = head
    while second and second.next:
        first = first.next
        second = second.next.next
    return first
```

## Reverse Linked List

https://leetcode.com/problems/reverse-linked-list/

```python
print('Hello world!')
```
