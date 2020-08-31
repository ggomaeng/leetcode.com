Author: @michaeldsdomingo

Date: August 30, 2020

# Attempt 3

/*

 * Definition for singly-linked list.
 * function ListNode(val, next) {
 *     this.val = (val===undefined ? 0 : val)
 *     this.next = (next===undefined ? null : next)
 * }
 */
/**
 * @param {ListNode} l1
 * @param {ListNode} l2
 * @return {ListNode}
 */

var addTwoNumbers = function(l1, l2) {
    var sum = new ListNode();
    var current = sum;
     
    do {
        let val1 = l1 ? l1.val : 0;
        let val2 = l2 ? l2.val : 0;

        current.val = current.val + val1 + val2;

        l1 = l1 ? l1.next : null;
        l2 = l2 ? l2.next : null;

        if (current.val >= 10) {
            current.val = current.val % 10;
            current.next = new ListNode(1);
        } else {
            current.next = l1 || l2 ? new ListNode() : null;
        }


        current = current.next;
    } while (l1 || l2);

    return sum;
};

Time Complexity: O(max(m,n))

Space Complexity: O(max(m,n))


# Solution 1

public ListNode addTwoNumbers(ListNode l1, ListNode l2) {
    ListNode dummyHead = new ListNode(0);
    ListNode p = l1, q = l2, curr = dummyHead;
    int carry = 0;
    while (p != null || q != null) {
        int x = (p != null) ? p.val : 0;
        int y = (q != null) ? q.val : 0;
        int sum = carry + x + y;
        carry = sum / 10;
        curr.next = new ListNode(sum % 10);
        curr = curr.next;
        if (p != null) p = p.next;
        if (q != null) q = q.next;
    }
    if (carry > 0) {
        curr.next = new ListNode(carry);
    }
    return dummyHead.next;
}