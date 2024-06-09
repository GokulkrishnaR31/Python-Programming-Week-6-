# Python-Programming-Week-6
1.Count Chars

Write a python program to count all letters, digits, and special symbols respectively from a given string







CODE:

n=input()

c1=0

c2=0

c3=0

for i in n:

    if i.isalpha():

        c1=c1+1

    elif i.isdigit():

        c2=c2+1

    else:

        c3=c3+1



print(c1)

print(c2)

print(c3)
#2.Decompress the String

Assume that the given string has enough memory. Don't use any extra space(IN-PLACE)





CODE:

s=[]

s1=[]

a=input()

for i in range(len(a)):

    

    if (len(s)==2):

        c=""

        k=s.pop(0)

        for m in s1:

            c+=str(m)

        s1=[]

        o=int(c)

    

        print(k*o,end="")

    if (a[i]>="a" and a[i]<='z'):

        s.append(a[i])

    elif(a[i]>='0' and a[i]<='9'):

        s1.append(a[i])

h=""

for j in range(len(s1)):

    h+=s1[j]

y=int(h)

print(s.pop(0)*y)
#3.First N Common Chars

Two string values S1, S2 are passed as the input. The program must print first N characters present in S1 which are also present in S2.

CODE:



S1 = input()

S2 = input()

N=int(input())

common_chars = set()



for char in S1:

    if char in S2:

        common_chars.add(char)



print(''.join(sorted(common_chars)[:N]))
#4.Remove Characters

Given two Strings s1 and s2, remove all the characters from s1 which is present in s2.



Constraints

1<= string length <= 200





CODE:

n1=input()

n2=input()



n=len(n1)

a=len(n2)

s=""

for i in n1:

    if(not(i in n2)):

        s+=i
print(s)           
#5.Remove Palindrome Words

String should contain only the words are not palindrome.



Sample Input 1

Malayalam is my mother tongue



Sample Output 1

is my mother tongue



CODE:

a=input()

a=a.lower()

b=a.split(' ')

#print(b)



for i in range(len(b)):

 p=b[i]

 if p!=p[::-1]:

  print(p,end=' ')
#6.Return Second World in Uppercase

Write a program that takes as input a string (sentence), and returns its second word in uppercase.



For example:



If input is “Wipro Technologies Bangalore” the function should return “TECHNOLOGIES”

If input is “Hello World” the function should return “WORLD”

If input is “Hello” the program should return “LESS”



NOTE 1: If input is a sentence with less than 2 words, the program should return the word “LESS”.

NOTE 2: The result should have no leading or trailing spaces.





CODE:



a=input()

b=a.split(" ")

if len(b)>=2:

 print(b[1].upper())

else:

 print("LESS") 


 #7. Reverse String

Reverse a string without affecting special characters. Given a string S, containing special characters and all the alphabets, reverse the string without affecting the positions of the special characters.

CODE:

s=input()

L=[]

for k in s:

    L.append(k)

j=len(L)-1

i=0

while(not(i==j)):

    if(L[i].isalnum()):

        while(not(L[j].isalnum())):

            j-=1

        temp=L[i]

        L[i]=L[j]

        L[j]=temp

        j-=1

        i+=1

    else:

        i+=1

        continue

s=""

for k in L:

    s+=k

print(s)
#8. String characters balance Test



Write a program to check if two strings are balanced. For example, strings s1 and s2 are balanced if all the characters in the s1 are present in s2. The character’s position doesn’t matter. If balanced display as "true" ,otherwise "false".





 CODE:

def are_strings_balanced(s1, s2):

    set_s1 = set(s1)

    set_s2 = set(s2)

    if set_s1 == (set_s1 & set_s2):

        return True

    else:

        return False

s1 = input().strip()

s2 = input().strip()

print(are_strings_balanced(s1, s2))
#9. Unique Names



In this exercise, you will create a program that reads words from the user until the user enters a blank line. After the user enters a blank line your program should display each word entered by the user exactly once. The words should be displayed in the same order that they were first entered. For example, if the user enters:



CODE:

s=input()

to_print=[]

while(not(s)==" "):

    to_print.append(s)

    s=input()

printed=[]

for x in to_print:

    if(not(x in printed)):

        print(x)

        printed.append(x)

    else:

        continue
#10. Username Domain Extension

Given a string S which is of the format USERNAME@DOMAIN.EXTENSION, the program must print the EXTENSION, DOMAIN, USERNAME in the reverse order.



Input Format:

The first line contains S.



Output Format:

The first line contains EXTENSION.

The second line contains DOMAIN.

The third line contains USERNAME.



Boundary Condition:

1 <= Length of S <= 100





CODE:

S=input()

d=S.find(".")

at=S.find("@")

print(S[d+1:])

print(S[at+1:d])

print(S[:at])



 
