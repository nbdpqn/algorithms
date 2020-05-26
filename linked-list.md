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
print('Hello world!')
```

## Palindrome Linked List

https://leetcode.com/problems/palindrome-linked-list/

```python
def reverseList(self, head: ListNode) -> ListNode:
    prev = None
    current = head
    while current:
        temp = current.next
        current.next = prev
        prev = current
        current = temp
    return prev


def isEqual(self, first: ListNode, second: ListNode) -> bool:
    while second:
        if second.val != first.val:
            return False
        second = second.next
        first = first.next
    return True


def isPalindrome(self, head: ListNode) -> bool:
    if not head or not head.next:
        return True
    prev = None
    slow = head
    fast = head

    while fast.next and fast.next.next:
        prev = slow
        slow = slow.next
        fast = fast.next.next
    
    secondHalf = slow.next
    if fast.next: # even length
        slow.next = None
        firstHalf = self.reverseList(head)
    else: # odd length
        prev.next = None
        firstHalf = self.reverseList(head)
    return self.isEqual(firstHalf, secondHalf)
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
