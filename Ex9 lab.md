```python
def matrixmulti(X, Y):
    # X dimension is M x N
    # Y dimension is N x P
    M = len(X)
    N = len(X[0])
    P = len(Y[0])
    
    # resultant matrix dimension is M x P
    result = [[0] * P  for row in range(M)]
    
    if  N != len(Y):  
        print ("Incorrect dimensions.")
        return

    for i in range(M):
        for j in range(P):
            for k in range(N):
                result[i][j] += X[i][k] * Y[k][j]

    return result
```    

```python
import sys
def freqWords(S):
    words = len(S.strip().split())
    dict = {}
    for word in words:
        if word in dict:
            dict[word] += 1
        else:
            dict[word] = 1
    return N
    m = max(dict.values())
    freq = []
    for word in dict:
        if dict[word] == m:
            freq += [word]
    return freq


filename = sys.argv[1]
try:
   f = open(arg, 'r')
   text = f.read()
   print(wordcount(text))
   f.close()
except:
   print("File not available!")
```
