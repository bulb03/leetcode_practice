```python
def kthGrammar(self, N, K):
    """
    :type N: int
    :type K: int
    :rtype: int
    """
    if(N==1):
        return 0
    else:
        if(K%2): #奇數=左子節點
            ans = self.kthGrammar(N-1,(K+1)/2)
            if(ans): #如果父節點是0，左子節點是0
                return 1
            else:
                return 0                
        else: #偶數=右子節點
            ans = self.kthGrammar(N-1,K/2)
            if(ans): #如果父節點是1，右子節點是0
                return 0
            else:
                return 1
# 找父節點的方式有誤，所以費了一番功夫
```