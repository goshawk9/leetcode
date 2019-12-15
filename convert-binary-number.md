# Problem

Convert Binary Number in a Linked List to Integer

# solution

```
/**
 * Definition for singly-linked list.
 * function ListNode(val) {
 *     this.val = val;
 *     this.next = null;
 * }
 */
/**
 * @param {ListNode} head
 * @return {number}
 */
var getDecimalValue = function(head) {
    result = 0;
    while (head !== null) {
        result = result*2 + head.val
        head = head.next
    }
    return result
};
```
