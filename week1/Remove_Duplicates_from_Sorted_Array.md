# Remove Duplicates from Sorted Array
### Solution code:
```
public class Solution {
    public int removeDuplicates(int[] nums) {

        int start = 1;

        for (int i = 0; i < nums.length - 1; i++) {
            if (nums[i] == nums[i+1]) {
                continue;
            }

            nums[start++] = nums[i+1];
        }
        
        return start;
    }
}
```

### Test case:
```
[-1,0,0,0,0,3,3]
[1,2,3,4,5]
[0,0,0,1,1,2,3]
[-1,-1,-2,-3,-4]
[1]
```
![pic](https://github.com/hpnhxxwn/cs501/blob/master/week1/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202017-06-04%20%E4%B8%8B%E5%8D%884.44.49.png?raw=true)
