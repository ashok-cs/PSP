### Simple exercises using modulo operator
- Write a function `isEven(N)` to find whether N is even or not.
```
eg: N = 9   returns  '9 is odd'
```
- Write a function `getEven(N)` to print even numbers upto N.
```
eg: N = 10   returns [2, 4, 6, 8, 10]
```
- Write a function `dec2bin(N)` to convert the decimal number N to its binary representation (in string).
```
eg: N = 12   binary_equivalent = 'b1100'
```
- Write a function `sum_digits(N)` to find the sum of all digits of N.
```
eg:  N = 12345   sum = 1 + 2 + 3 + 4 + 5 = 9
```
- Write a function `sum_odd_digits(N)` to find the sum of all the digits in the odd positions of N.
```
eg:  N = 12345    sum_odd_digits = 1 + 3 + 5 = 9
```

### Round with modulo
- Write a function `ceil10(N)` to round the given N to the nearest **upper** multiple of 10s. 
```
eg:  N = 122    ceil10 = 130
```
- Write a function `floor10(N)` to round the given N to the nearest **lower** multiple of 10s. 
```
eg:  N = 122    floor10 = 120
```
- Write a function `round10(N)` to round the given N to the **nearest** multiple of 10s. 
```
eg:  N = 122    floor10 = 120
```
- Write a function `check(N, M)` to check whether N is the multiple of M
```
eg:  N = 122 M=3    returns   False
```
- Write a function `add_rem_235(N)` to add all the reminders when N is divided by 2, 3 and 5 respectively.
```
eg: N = 122     N % 2 = 0  N % 3 = 2  N % 5 = 2   returns  0 + 2 + 2 = 4
```

### From CodingBat
- Return true if the given non-negative number is special. Use the % "mod" operator 
```
specialEleven(22) → true
specialEleven(23) → true
specialEleven(24) → false
```
- Return true if the given non-negative number is a multiple of 3 or 5, but not both. Use the % "mod" operator 
```
old35(3) → true
old35(10) → true
old35(15) → false
```
- Return true if the given non-negative number is 1 or 2 more than a multiple of 20. 
```
more20(20) → false
more20(21) → true
more20(22) → true
```
- Return true if the given non-negative number is 1 or 2 less than a multiple of 20. So for example 38 and 39 return true, but 40 returns false. 
```
less20(18) → true
less20(19) → true
less20(20) → false
```
- Given a non-negative number "num", return true if num is within 2 of a multiple of 10. Note: (a % b) is the remainder of dividing a by b, so (7 % 5) is 2. 
```
nearTen(12) → true
nearTen(17) → false
nearTen(19) → true
```
### Write a function `time_elapsed(start, end)` to find the time elapsed in minutes.
```
eg: 7:04 AM, 7:28 AM   time_elapsed = 24 minutes
```

