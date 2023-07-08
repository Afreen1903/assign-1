# assignment-1
# avg finding:-
if __name__ == '__main__':

    n = int(input())

    student_marks = {}

    for _ in range(n):

        name, *line = input().split()

        scores = list(map(float, line))

        student_marks[name] = scores

    query_name = input()

    l1 = list(student_marks[query_name]) 

    addition = sum(l1)

    result = addition/len(l1)

    print('%.2f'% result)

    # string split and join:-

    def split_and_join(line):

    # write your code here

    a = line.split(" ")

    b = "-".join(a)

    return(b)


if __name__ == '__main__':

    line = input()

    result = split_and_join(line)

    print(result)

  # set.intersection operation:-

  eng = set()
fre = set()
n = raw_input()
for i in raw_input().split(' '):
  eng.add(i)
m = raw_input()
for i in raw_input().split(' '):
  fre.add(i)
sol = eng.union(fre)
print len(sol)

# finding runner up score

if __name__ == '__main__':
    n = int(input())
    arr = list(map(int, input().split()))
    arr1 = set(arr)
    arr2 = sorted(arr1)
    print(arr2[-2])

# swap case problem:-

def swap_case(s):

    string = ""

    for i in s:

        if i.isupper() == True:

            string+=(i.lower())

        else:

            string+=(i.upper())

    return string


if __name__ == '__main__':

    s = input()

    result = swap_case(s)

    print(result)

# Arithmetic Operators:-

if __name__ == '__main__':
    a = int(input())
    b = int(input())
    print(a+b)
    print(a-b)
    print(a*b)

# Division

if __name__ == '__main__':
    a = int(input())
    b = int(input())
    print(a//b)
    print(a/b)
# Python If-Else

#!/bin/python3

import math
import os
import random
import re
import sys



if __name__ == '__main__':
    n = int(input().strip())
    
    if n%2 != 0:
        print("Weird")
    elif n%2 == 0 and n>2 and n<=5:
        print("Not Weird")
    elif n%2 ==0 and n > 6 and n <=20:
        print("Weird")
    else:
        print("Not Weird")

  # Nested Lists

  if __name__ == '__main__':
    alist = []
    for i in range(int(input())):
        name = input()
        score = float(input())
        alist.append([name, score])
second_highest = sorted(set([score for name, score in alist]))[1]
print('\n'.join(sorted([name for name, score in alist if score == second_highest])))

# Loops:-

if __name__ == '__main__':
    n = int(input())
    for i in range(n):
        print(i*i)

# leap year:-

def is_leap(year):
    
    # variable to check the leap year
    leap = False
    
    # divided by 100 means century year
    # century year divided by 400 is leap year
    if (year % 400 == 0) and (year % 100 == 0):
        
       # change leap to True
        leap = True

    # not divided by 100 means not a century year
    # year divided by 4 is a leap year
    elif (year % 4 ==0) and (year % 100 != 0):
        
        #Change leap to true
        leap = True

    #else not a leap year
    else:      
        pass
    
    return leap

# find a string:-

def count_substring(string, sub_string):
    total = 0
    for i in range(len(string)):
        if string[i:len(string)].startswith(sub_string):
            total += 1
    return total

if __name__ == '__main__':
    string = input().strip()
    sub_string = input().strip()
    
    count = count_substring(string, sub_string)
    print(count)

  # Lists:-

  if __name__ == '__main__':

    N = int(input())

    List=[];

    for i in range(N):

        command=input().split();

        if command[0] == "insert":

            List.insert(int(command[1]),int(command[2]))

        elif command[0] == "append":

            List.append(int(command[1]))

        elif command[0] == "pop":

            List.pop();

        elif command[0] == "print":

            print(List)

        elif command[0] == "remove":

            List.remove(int(command[1]))

        elif command[0] == "sort":

            List.sort();

        else:

            List.reverse();

