# Guess Number Higher or Lower


## **題目**
終極密碼，傳我們猜的答案到guess()這個函數裡

如果回傳0，代表找到了  
如果回傳-1，代表答案小於我們猜的  
如果回傳1，代表答案大於我們猜的

## **解決思維**
這題是放在binary search tree(BST)裡，所以我用BST的方式來解
```python
def guessNumber(self, n):
    """
    :type n: int
    :rtype: int
    """
    left = 1
    right = n
    
    while left<=right:
        ans = (left+right)/2
        if not guess(ans): # 0，找到答案了
            return ans
        elif guess(ans) == -1: # -1，答案小於我們猜的
            right = ans - 1
        else: # 1，答案大於我們猜的
            left = ans + 1
```
# **可能問題**
* 時間複雜度普通
* 空間複雜度普通
# **改良方法**