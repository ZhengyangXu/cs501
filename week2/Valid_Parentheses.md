# Valid Parentheses
### Solution code:
```
public class Solution {
    public boolean isValid(String s) {
        if (s == "")
            return true;
        
        ArrayDeque<Character> stack = new ArrayDeque<Character>();
        char[] c = s.toCharArray();
        for (int i = 0; i < c.length; i++) {
            if (c[i] == ')' || c[i] == '}' || c[i] == ']') {
                if (stack.isEmpty())
                    return false;
                char tmp = stack.pop();
                if ((c[i] == ')' && tmp != '(') || (c[i] == '}' && tmp != '{') || (c[i] == ']' && tmp != '['))
                    return false;
            }
            else {
                stack.push(c[i]);
            }
        }
        return stack.isEmpty();
    }
}
```

### Test code:
```
"["
```
```
"[]"
```
```
""
```
```
()[]{}
```
```
([)]
```

![pic](https://github.com/hpnhxxwn/cs501/blob/master/week2/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202017-06-10%20%E4%B8%8B%E5%8D%886.37.02.png?raw=true)
