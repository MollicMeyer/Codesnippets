# Codesnippets
## Code without a home :house:
#### Python v 2.7

#### Trapezoidal interpolation base function for interpolating soil properties through depth. Still working out the semantics. 
```
def Trapezoidal(f, a, b, n):
    h = (b-a)/float(n)
    s = 0.5*(f(a) + f(b))
    for i in range(1,n,1):
        s = s + f(a + i*h)
    return h*s

