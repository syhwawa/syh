1. 应该是随机的。我考的第一道是sum input，从1开始加到input的数字，但要剔除可以被5或7整除的数；第二道是输出input句子里最长的单词
Sum the number from 1 to n, remove the number is  divisible by 5 and 7.

```Python
def sum_input(n):
    res = 0
    for i in range(1,n+1):
        if i % 5 != 0 and i % 7 !=0:
            res += i 
    return res
n = 18
sum_input(n)
```

2. 第二道是输出input句子里最长的单词

def long_word(s):
    n = max(s.split(), key=len)
    max_len = len(n)
    return (n, max_len)

s = "I am an intern at geeksforgeeks, but i am xxasfasf, how are geeksforgeekslol."
long_word(s)

```Python
def longest_word(filename):
    with open(filename, 'r') as infile:
              words = infile.read().split()
    max_len = len(max(words, key=len))
    return [word for word in words if len(word) == max_len]

print(longest_word('test.txt'))
```

3. Given an integer, find the sum of its digits. 
```Python
def add_digits(n):
    res = 0
    while n:
        res += n % 10
        n = n // 10
    return res

add_digits(943)
```

4. Given a list of integers, find the largest difference between them.

```Python
def maxdiff(arr):
    max_diff = arr[1] - arr[0]
    min_element = arr[0]
    
    for i in range(1, len(arr)):
        if max_diff < arr[i] - min_element:
            max_diff = arr[i] - min_element
        
        if  arr[i] < min_element:
            min_element = arr[i]
        
    return max_diff
    
arr = [2, 90, 10, 110] 
maxdiff(arr)
```

https://www.geeksforgeeks.org/maximum-difference-between-two-elements/

```Python
array = [45,3,8,1,2,19,22,35,23]
new = sorted(array,reverse=False)

A = new[0]

while True:
    B = new[-1]
    if array.index(B) > array.index(A):
        print A,B
        break
    else:
        new.remove(B)
```


5.Reverse:
Input:Hello World
Output:World Hello

```
def reverse_string(s):
    r = ' '.join(reversed(s.split(' ')))
    return r

s = 'you shall not pass'
reverse_string(s)
```
https://medium.com/@hmurari/a-popular-programming-interview-question-reverse-words-of-a-sentence-3bac606d15a2

6. 
calculate_distance(p1, p2)
input p1 = (1,2), p2 = (4, -2)
output 5

import math
def calculate_distance(p1, p2):
    return int(math.sqrt((p1[0]-p2[0])** 2 + (p1[1]-p2[1]) ** 2))

p1 = (1,2)
p2 = (4, -2)
calculate_distance(p1, p2)
import math 
  
# Function to calculate distance 
def distance(x1 , y1 , x2 , y2): 
  
    # Calculating distance 
    return math.sqrt(math.pow(x2 - x1, 2) +
                math.pow(y2 - y1, 2) * 1.0) 
  
# Drivers Code 
print("%.6f"%distance(3, 4, 4, 3)) 
