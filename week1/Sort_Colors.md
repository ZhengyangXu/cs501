# Sort Colors
### Solution code:
```
public class Solution {
    public static int red = 0;
    public static int white = 1;
    public static int blue = 2;
    public void sortColors(int[] nums) {
        int p1 = 0;
        int p2 = nums.length - 1;
        
        for (int i = 0; i <= p2; i++) {
            while (nums[i] == 2 && i < p2) {
                int tmp = nums[i];
                nums[i] = nums[p2];
                nums[p2--] = tmp;
            }
            while (nums[i] == 0 && i > p1) {
                int tmp = nums[i];
                nums[i] = nums[p1];
                nums[p1++] = tmp;
            }
        }
        
    }
}
```

### Test case:
```
[0]
[0,1,0,2,0,1,2,2,1,1]
[1,0]
[1,0,0,2,2,2,0]
[2,0,0,2,2,2,1]
```

![pic](https://github.com/hpnhxxwn/cs501/blob/master/week1/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202017-06-04%20%E4%B8%8B%E5%8D%884.53.31.png?raw=true)
