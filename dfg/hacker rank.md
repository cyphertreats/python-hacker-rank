# python-hacker-rank
#### integer division
```
if __name__ == '__main__':
    a = int(input())
    b = int(input())
    print (a//b)
    print (a/b)
```
#### range 
```
if __name__ == '__main__':
    n = int(input())
    for i in range (n):
        print (i+1, end="")
```
#### Fast Inverse Square Root
```
from ctypes import c_float, c_int32, cast, byref, POINTER

def ctypes_isqrt(number):
    threehalfs = 1.5
    x2 = number * 0.5
    y = c_float(number)

    i = cast(byref(y), POINTER(c_int32)).contents.value
    i = c_int32(0x5f3759df - (i >> 1))
    y = cast(byref(i), POINTER(c_float)).contents.value

    y = y * (1.5 - (x2 * y * y))
    return y
number = int(input("Enter the number= "))
ctypes_isqrt(number)
```
