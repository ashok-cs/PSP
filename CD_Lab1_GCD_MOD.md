# Problems using Modulo operator

### http://cyberdojo1.kgfsl.com/enter/show/3A61E9

- Write a function `check(N, M)` to check whether N is the multiple of M
```
eg:  N = 122 M=3    returns   False
```

###  http://cyberdojo1.kgfsl.com/enter/show/5D793C
- Write a function `add_rem_235(N)` to add all the reminders when N is divided by 2, 3 and 5 respectively.
```
Write a function `add_rem_235(N)` to add all the reminders 
when N is divided by 2, 3 and 5 respectively.

eg: 
N = 122     
N % 2 = 0  
N % 3 = 2  
N % 5 = 2  

    The function returns  0 + 2 + 2 = 4
```

### http://cyberdojo1.kgfsl.com/enter/show/D18E54
- Write a function `isEven(N)` to find whether N is even or not.
```
eg: N = 9   returns  True
```
- Write a function `getEven(N)` to print even numbers upto N.
```
eg: N = 10   returns [2, 4, 6, 8, 10]
```

### http://cyberdojo1.kgfsl.com/enter/show/8F5ED1

- Write a function `sum_digits(N)` to find the sum of all digits of N.
```
eg:  N = 12345   sum = 1 + 2 + 3 + 4 + 5 = 9
```
- Write a function `sum_odd_digits(N)` to find the sum of all the digits in the odd positions of N.
```
eg:  N = 12345    sum_odd_digits = 1 + 3 + 5 = 9
```

### http://cyberdojo1.kgfsl.com/enter/show/90C018

- Write a function `ceil10(N)` to round the given N to the nearest **upper** multiple of 10s. 
```
eg:  N = 122    ceil10 = 130
```
### http://cyberdojo1.kgfsl.com/enter/show/C66954
- Write a function `floor10(N)` to round the given N to the nearest **lower** multiple of 10s. 
```
eg:  N = 122    floor10 = 120
```
### http://cyberdojo1.kgfsl.com/enter/show/EBCAA2
- Write a function `round10(N)` to round the given N to the **nearest** multiple of 10s. 
```
eg:  N = 122    round10 = 120
```

### http://cyberdojo1.kgfsl.com/enter/show/147399

- Write a function `dec2bin(N)` to convert the decimal number N to its binary representation (in string).
```
eg: N = 12   binary_equivalent = 'b1100'
```
### http://cyberdojo1.kgfsl.com/enter/show/DCFA73
Write a function to check whether given year is leap or not.

Solution:
- A year is a leap year, if it is divisible by 4 and not by 100
- A year is a leap year, if it is divisible by 400

Example:
```
isLeap(2000) --> True
isLeap(2100) --> False
isLeap(2016) --> True
```

### http://cyberdojo1.kgfsl.com/enter/show/BE76D5
Write a function to find the number of days for the given month and the year.

Note:
You need to find out whether given year is leap or not,
before finding the number of days.

```
Example:
days(2, 2012)  -->  29  # as 2012 is the leap year
days(4, 2010)  -->  30
days(10, 2017) -->  31
```

# Advanced problems

### http://cyberdojo1.kgfsl.com/enter/show/AF85FC 

Find the GCD of the sums of digits of two numbers. 

Example: 

input: 234, 456 

sum1 = 2 + 3 + 4 = 9 
sum2 = 4 + 5 + 6 = 15 

gcd(sum1,sum2) = 3 

Lab1: GCD 

### http://cyberdojo1.kgfsl.com/enter/show/07274F 

There are 'x' male students and 'y' female students studying in a class. 
We need to form students teams of equal size. Teams shall not have the 
mix of boys and girls. The team size shall not exceed 5. 

Write a function to find the minimum number of teams that can be formed. 

ADDITIONAL CLARIFICATIONS: 

1. When forming teams, no student must be left behind, meaning 

every student must be assigned to a team. 

2. The team size of both females and males chosen must not be 

be the same. 


Example: 
In a classroom, there are '10' boys and '20' girls. 
Condition: 
1. Teams should be of equal size. 
2. The team size shall not exceed 5. 

For a team of '5' members, we will have 6 teams. 
For a team of '2' members, we will have 15 teams. 
For a team of '10' members, we will have 3 teams. 

As team size can not exceed 5, you need to return '6' as the 
minimum teams that can be formed with equal size. 



# codingbat.com

### http://codingbat.com/prob/p100962

- We'll say a number is special if it is a multiple of 11 or if it is one more than a multiple of 11. Use the % "mod" operator 
```
specialEleven(22) → true
specialEleven(23) → true
specialEleven(24) → false
```
### http://codingbat.com/prob/p112564

- Return true if the given non-negative number is a multiple of 3 or 5, but not both. Use the % "mod" operator 
```
old35(3) → true
old35(10) → true
old35(15) → false
```

### http://codingbat.com/prob/p118290
- Return true if the given non-negative number is 1 or 2 more than a multiple of 20. 
```
more20(20) → false
more20(21) → true
more20(22) → true
```

### http://codingbat.com/prob/p133158
- Return true if the given non-negative number is 1 or 2 less than a multiple of 20. So for example 38 and 39 return true, but 40 returns false. 
```
less20(18) → true
less20(19) → true
less20(20) → false
```

### http://codingbat.com/prob/p193613
- Given a non-negative number "num", return true if num is within 2 of a multiple of 10. Note: (a % b) is the remainder of dividing a by b, so (7 % 5) is 2. 
```
nearTen(12) → true
nearTen(17) → false
nearTen(19) → true
```

