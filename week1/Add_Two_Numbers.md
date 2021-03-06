# Add Two Numbers
### Solution code:
```
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) { val = x; }
 * }
 */
public class Solution {
    public ListNode addTwoNumbers(ListNode l1, ListNode l2) {
        int sum = 0;
        ListNode res = new ListNode(0);
        ListNode dummy = res;
        while (l1 != null || l2 != null) {
            sum = sum/10;
            if (l1 != null) {
                sum += l1.val;
                l1 = l1.next;
            }
            if (l2 != null) {
                sum += l2.val;
                l2 = l2.next;
            }
            
            res.next = new ListNode(sum % 10);
            res = res.next;
        }
        
        sum = sum / 10;
        if (sum > 0) {
            res.next = new ListNode(sum);
        }
        
        return dummy.next;
    }
}
```

### Test case:
```
[2,4,3]
[5,6,4]
```
```
[2,4,6]
[5,6,4]
```
```
[]
[5,6,4]
```
```
[2,3,4]
[]
```
```
[]
[]
```

![pic](https://github.com/hpnhxxwn/cs501/blob/master/week1/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202017-06-04%20%E4%B8%8B%E5%8D%888.02.55.png?raw=true)
