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
def reorderList(self, head: ListNode) -> None:
    if not head:
        return head
    data = []
    current = head
    i, j = 0, -1
    while current:
        data.append(current)
        current = current.next
        j += 1
    while i < j:
        data[i].next = data[j]
        i += 1
        if i >= j:
            break
        data[j].next = data[i]
        j = j - 1
    data[j].next = None


def reorderList(self, head: ListNode) -> None:
    if not head:
        return head

    mid = head
    temp = head
    while mid.next and temp.next and temp.next.next:
        mid = mid.next
        temp = temp.next.next

    tail = mid
    previous = None
    half = mid.next
    while half:
        mid.next = previous
        previous = mid
        mid = half
        half = half.next
    mid.next = previous
    current = None
    while current != tail:
        current = head.next
        head.next = mid
        head = mid
        mid = current
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
