# Letter Combinations of a Phone Number
### Solution code:
```
public class Solution {
    public List<String> letterCombinations(String digits) {
        if (digits == null || digits.length() == 0)
            return new ArrayList<String>();
            
        String[] map = new String[] {"0", "1", "abc", "def", "ghi", "jkl", "mno", "pqrs", "tuv", "wxyz"};
        
        char[] c = digits.toCharArray();
        LinkedList<String> res = new LinkedList<String>();
        res.add("");
        for (char i: c) {
            int size = res.size();
            for (int k = 0; k < size; k++) {
                String t = res.removeFirst();
                char[] tmp = map[i - '0'].toCharArray();
                for (char j: tmp) {
                    res.add(t + j);
                }
            }
        }
        
        return res;
    }
}
```

### Test case:
```
""
```
```
"2"
```
```
"1"
```
```
"01"
```
```
"23"
```

![pic](https://github.com/hpnhxxwn/cs501/blob/master/week2/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202017-06-12%20%E4%B8%8B%E5%8D%8810.15.25.png?raw=true)
