# Palindrome Number

## **題目**
中文就是指：迴文，EX：上海自來水來自海上

從頭唸到尾和從尾念到頭都是一樣的

## **解決思維**
將它換成string，再一一比較
## **程式碼**
* python
```python
    def isPalindrome(self, x):
        y = str(x)
        
        start = 0
        last = len(y)-1
        
        while last > start:
            if(y[start]==y[last]):
                start += 1
                last -= 1
            else:
                return False
        return True
```
# **可能問題**
* 空間複雜度過高
* 時間複雜度過高，O(n)
# **改良方法**
* 減少空間複雜度