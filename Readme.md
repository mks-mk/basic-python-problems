[![License:MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

# 100+ Basic-Python-Problems


## Qn1: *write a program to calculate the area of a circle of radius "r" entered by user*

### solution:
```python
r=float(input("Enter the radius:"))
pi=3.14
if r==0:
    print("Enter a non zero value")
else:
    print("Area of the given circle=",pi*r**2)
```
## Qn2: *Reverse the user's name*

### solution:
```python
a=input(("enter your first name:"))
b=input(("enter your last name:"))
print("reversed name:",b+" "+a)
```
## Qn3: *Write a Python program that accepts an integer (n) and computes the value of n+nn+nnn.*

### solution:
```python
a=int(input("Enter your number: "))
n1=int(str(a)*1)
n2=int(str(a)*2 ) 
n3=int(str(a)*3)
print(n1+n2+n3)

#str() converts any value to string.variables n1,n2,n3 are created by converting the input integer "a" to a string and then back to an integer
```
## Qn4: *A script that calculates n+nn+nnn but allows the user to input any number of repetitions.*

### solution:
```python
a=int(input("enter the integer: "))
n1=int(str(a)*int(input("enter the 1st rept value")))
n2=int(str(a)*int(input("enter the 2nd rept value")))
n3=int(str(a)*int(input("enter the 3rd rept value")))
print(n1+n2+n3)
```
## Qn5: *python program to calculate the difference between a given number and 17.If the number is greater than 17 return twice the absolute difference*
### solution:
```python
n=int(input("Enter your number: "))
def dis(c):  
    if c>=17:
        return (c-17)*2
    else:
        return (17-c)
a=dis(n) #called the function for the value n
print(a)
# 'dis' is a just a func name that i given, you can use any name, and the c can be any value
```
## Qn6: *Write a Python program to calculate the sum of three given numbers. If the values are equal, return three times their sum*
### solution':
```python
n1=int(input("enter your first number: "))
n2=int(input("enter your second number: "))
n3=int(input("enter your third number: "))
a=n1+n2+n3
if (n1==n2==n3):
    
    print("since the numbers are equal-->",a*3)
else:
    print("since the numbers are not equal--> ",a)
```
## Qn7: *Program to get the volume of a sphere with radius six*
### solution:
```python
radius=6
pi=3.14 # you can import math to get more accurate pi value
volume=4/3*pi*radius**3
print("volume of sphere with radius 6= ",volume)
```
## Qn8: *Program that determines whether a given number (accepted from the user) is even or odd, and prints an appropriate message to the user*
### solution:
```python
number=int(input("Enter your number: "))
if number%2==0:
    print("The given number is even")
else:
    print("The given number is odd")
```
## Qn9: *program to test whether a passed letter is a vowel or not which is entered by user*
### solution:
```python
def isvowel(letter):
    vowels="aeiou"
    if letter in vowels:
        print(letter, "is vowel")
    else:
        print(letter, "is not vowel")
character=str(input("Enter your character: "))
isvowel(character)
```
## Qn10: *program that will accept the base and height of a triangle and compute its area.*
### solution:
```python
base=float(input("Enter the base: "))
height=float(input("Enter the height: "))
area=1/2*base*height
print("Area of the triangle= ",area)
```
## Qn11: *Program that computes the greatest common divisor/ highest common facor(HCF) of two positive integers*
### solution:
```python
def hcf(x,y):
    if x%y==0:
        return y
    for i in range(int(y),0,-1):
        # y might be a float, so int() ensures it’s converted to an integer.
        # The HCF (Highest Common Factor) of two numbers can never be greater than the smaller number (y in this case).
        
        #In fact, it also can’t be greater than half of that smaller number — except when one number divides the other exactly.but here i didn't applied that, ie y/2

        if x%i==0 and y%i==0:
            a=i
            return a
n1=int(input("Enter your first no. "))
n2=int(input("Enter your second no. "))
var=hcf(n1,n2) 
print(var,"is the hcf")
```
## Qn12: *Program to sum two given integers. However, if the sum is between 15 and 20 it will return 20,the numbers are entered by the user.*
### solution:
```python
def function(a,b):
    sum=a+b
    if sum>15 and sum<20:
        return 20
    else:
        return sum
n1=int(input("Enter your first number"))
n2=int(input("Enter your second number"))
a=function(n1,n2)
print(a)
```
## Qn13: *Program that returns true if the two given integer values are equal or their sum or difference is 5.*
### solution:
```python
a=int(input("enter your first number: "))
b=int(input("enter your second number: "))
if a==b or a+b==5 or abs(a-b)==5: # abs make a-b always positive
    print("True")
else:
    print("False")
```
## Qn14: *Program that displays your name, age, and address on three different lines.*
### solution:
```python
def data():
    name, age,adress="Mksinan",99,"kerala" 
    print("name:{}\nage:{}\naddress:{}".format(name,age,adress))   #curly braces {} are placeholders for the values that will be passed through the .format() method.
data()
```
## Qn15: *program to parse a string to float or integer.*
### solution:
```python
n=input("Enter the number: ")
print(float(n))
print(int(float(n)))
```
## Qn16: *Write a Python program to print without a newline or space.*
### solution
```python
#The problem is,when you use the print() function in Python, by default it moves to a new line after printing.But here, you’re asked to print several outputs on the same line, without spaces or line breaks between them.
#The end="" tells Python don't move to the next line after printing.
for i in range(0,10):
    print("HI",end="") #without the 'end=' the outputs will be in newlines,can insert anything between the end="(can be anything here)"
```
## Qn17: *Program to sum the first n positive integers.*
### solution:
```python
# Equation to find the sum of first n positive integers :
#          sum=[n(n+1)]/2
n=int(input("Enter your number: "))
sum=(n*(n+1))/2
print("Sum of the first",n,"positive integers: ",sum)
```
## Qn18: *Program to convert height in feet and heiht in  inches to centimeters.*
### solution:
```python
print("Input your Height in")
hfeet=int(input("feet: "))
hinch=int(input("inches: "))
H=hfeet+(hinch/12)
hcm=H*30.48
print(f"Your height in cm is = {hcm}") # simply, ' f {} ' are used to easily insert variables or expressions inside strings. Just to make look cleaner and easy
```
## Qn19: *Program to convert all units of time into seconds*
### solution:
```python
print("input the time in: ")
days=int(input("Input days= "))*86400
hour=int(input("Input time in hrs= "))*3600
min=int(input("Input time in min= "))*60
sec=int(input("Input time in sec= "))
res=days+hour+min+sec
print(f"The amount of seconds = {res}")
```
## Qn20: *Program that converts that amount of seconds into days, hours, minutes*
### solution:
```python
sec=int(input("Input the amount of seconds : "))
days=sec//86400 #gives an integer value,ie a full day,the fraction parts (got when dividing the inputed seconds by 86400)contain hours,minutes,and seconds
reminding_sec=sec%86400
hours=reminding_sec//3600
reminding_sec2=reminding_sec%3600
minutes=reminding_sec2//60
reminding_sec3=reminding_sec2%60
seconds=reminding_sec3
print(f"{days}d,{hours}h,{minutes}m,{seconds}s")
```
## Qn21: *Program to calculate sum of digits of a number.*
### solution:
```python
n=int(input("Enter your number : ")) #loop variable initialisation
sum=0
i=n # i used n as i in loop for display the n at last
while i>0: # condition for while loop termination,here loops works until n<0
    a=i%10
    sum+=a
    i=i//10 # loop variable initialisation
print(f"sum of digits of \"{n}\" = {sum}")
```
## Qn22: *program to compute the sum of digits of a number using recursion.*
### solution:
```python
def sum_of_digits(a):
    if a==0:
        return 0
    else:
        if a>0:
            return (a%10)+ sum_of_digits(a//10)
n=int(input("Enter your number: "))
print("sum of digits of",n,"= ",sum_of_digits(n))
```
## Qn23: *Program to check if the sum of digits of a number is an even or odd number.*
### solution:
```python
n=int(input("Enter your number: "))
sum_of_digits=0
while n>0:
    digits=n%10
    sum_of_digits+=digits
    n=n//10
if sum_of_digits%2==0:
    print("Sum of digits is even : ",sum_of_digits)
else:
    print("Sum of digits is odd : ",sum_of_digits)
```
## Qn24: *Program to find the product of digits of a number*
### solution:
```python
n=int(input("Enter your number: "))
product_of_digits=1 #if this variable set as 0, the entire output will be zero, 0*anything=0
while n>0:
    digits=n%10
    product_of_digits*=digits
    n=n//10
print("Product of digits= ", product_of_digits)
```
## Qn25: *program to sort three integers without using conditional statements and loops.*
### solution:
```python
n1=int(input("Input first number: "))
n2=int(input("Input second number: "))
n3=int(input("Input third number: "))
x=min(n1,n2,n3) # find the min value among n1,n2,n3
y=max(n1,n2,n3) # find the max value among n1,n2,n3
z=(n1+n2+n3)-(x+y) # calculating the third value, ie the middle number, bcz we already know first number min value, and last number max value
print("Numbers in sorted order: ",x,z,y)
```
## Qn26: *program to print daimond shaped star pattern, number of raws are entered by the user*
### solution:
```python
n=int(input("Enter your number of rows:"))
for i in range(0,n+1): # the first line of the output will be a collection of spaces, bcz the range given for i starts from 0. you can also give 1, so the first line of output will be a star
    print(" "*(n-i),end="")
    print("*"*(2*i-1)) # here the expression (2*!-1) represents all odd numbers, buy changing the expression only, we can print more different patterns
for i in range((n-1),0,-1):
    print(" "*(n-i),end="")
    print("*"*(2*i-1))
```
## Qn27: *Python program to display only those numbers from a list that satisfy the following conditions*

- The number must be `divisible by five`
- If the number is `greater than 150`, then `skip it` and move to the following number
- If the number is `greater than 500`, then `stop the loop`

### solution:
```python
list=[12, 75, 150, 180, 145, 525, 50] .
for i in list:
    if i>500:
        break #break stops the entire loop immediately.The loop ends here no further numbers are checked.
    elif i>150:
        continue  #Meaning of continue:It skips the rest of the code inside the loop for this iteration and moves to the next number.
        print("hI")
    elif i%5==0:
        print(i)

#output 75 150 145
```
## Qn28: *Prime numbers within a range eg b/w 25 and 50*
### solution:
```python
for i in range(25,51):
    if i >1:
        for num in range(2,i):
            if i%num==0:
                break # if this condition become false after checking every numbers from 2 to i-1 , the code will execute from outside of the "if".
        else:
            print(i)
```
## Qn29: *Fibonacci series up to 10 terms*
### solution:
```python
a=0
b=1 #in Fibonacci series, each number=sum of two previous numbers, thats why we start with 0 and 1
for i in range(10):
    print(a)
    a = b
    b = a+b
```
## Qn30: *Program to find factorial of a given number using for loop*
### solution:
```python
n=int(input("Enter your number:"))
factorial=1
if n==0:
    print("factorial: ",1)
elif n<0:
    print("factorial does not exist")
else:
    for i in range(1,n+1):
        factorial*=i

    print("factorial of the number", factorial)
```
## Qn31: *Reverse a integer number*
### solution:
```python
n=int(input("Enter your number: "))
reversed_no=0
while n >0:
    a=n%10
    reversed_no=reversed_no*10 +a #if there is no '*10' it just gives sum of digits
    n=n//10

print("Reversed number: ",reversed_no)
```
## Qn32: *print elements present in the odd positions of the given list*
### solution:
```python
my_list=[1,2,3,4,5,6,6,7,8,8,8,8,9]
for i in my_list[1: :2]: # means, index[start:stop:step]
    print(i,end=",")
```
## Qn33: *Create a function that accepts a variable number of arguments and prints each of their values.*
### solution:
```python
def print_values(*args):
    print("printing values:")
    for i in args:
        print(i)
print_values(10,2,20,4,30,6)
```
## Qn34: *Write a function calculation() that accepts two variables and calculates both their addition and subtraction. The function should then return both the sum and the difference in a single return statement.*
### solution:
```python
def calculation(a,b):
    addition=a+b
    substraction=a-b
    return addition, substraction
result=calculation(23,3)
print("result=", result)
```
## Qn35: *Write a program to create a function show_employee() with the following specifications:*
 - It should accept the employee’s name and salary.
 - It should display both the name and salary.
 - If the salary is not provided in the function call, it should default to 9000.
 ### solution:
 ```python
def show_employee(name,salary=9000):
    print("name:", name," ", "salary:", salary)
show_employee("Mkzenova")
show_employee("Mkzenova", 400000)
```
## Qn36: *Create a program with nested functions to perform an addition calculation as follows:*
- Define an outer function that accepts two parameters, a and b.
- Inside this outer function, define an inner function that calculates the sum of a and b.
- The outer function should then add 5 to this sum.
- Finally, the outer function should return the resulting value.
```python
def outer_function(a,b):
    def inner_function(a,b):
        return a+b
    result=inner_function(a,b)
    return result+5
n1=int(input("Enter first number:"))
n2=int(input("Enter second number:"))
print(outer_function(n1,n2))
```
## Qn37: *Generate a Python list of all the odd numbers between 1 to 100*
### solution:
```python
print(list(range(1,100,2)))
```
## Qn38: *Find the largest item from the list user created*
### solution:
```python
list=[]
no_of_elements=int(input("Enter number of elements of list:"))
for i in range(0,no_of_elements):
    element=int(input("Enter the element:"))
    list.append(element)
print(list)
print("The largest item from the list is ",max(list))
```
## Qn39: *A recursive function to calculate the factorial of 5*
### solution:
```python
def factorial(a):
    if a==0:        #The function needs a condition to stop calling itself.ie base case, here this if condition is the base case
        return 1
    return a*factorial(a-1)
print(factorial(5))
```
## Qn40: *write a programme for recursive multiplication two positive integers*
### solution:
```python
def multiply(a,b):
    if b==0:
        return 0
    else:
        return a+ multiply(a, b-1)   #remember, multiplication means repeated addition,For example:
                                     # 5 × 3 = 5 + 5 + 5
                                     # So, if multiply(a, b) means "add a exactly b times".
n1=int(input("First positive number="))
n2=int(input("Second positive number="))
print("result=",multiply(n1,n2))
```
## Qn41: *programme to check if a triangle (using functions, side lengths are entered by user ) is right triangle or not*
### solution:
```python
def is_right_triangle(a,b,c):
    if a**2+b**2==c**2 or b**2+c**2==a**2 or a**2+c**2==b**2:   # Pythagoras theorem
        print("---Right triangle---")
    else:
        print("---Not right triangle---")
side1=int(input("Enter side length1:"))
side2=int(input("Enter side length2:"))
side3=int(input("Enter side length3:"))

is_right_triangle(side1,side2,side3)
```
## Qn42: *write a program to check if a given number is armstrong or not.*
`Hint: Armstrong number is a number that is equal to the sum of its own digits, each raised to a power equal to the number of digits in the number`
- eg: 153=1^3+ 5^3+ 3^3
### solution:
``` python
number=int(input("Enter your number:"))
temp=number       # we want to use the "number" in many places, so we must save a copy of the number to another variable 
no_of_digits=0
while number>0:
    digit=number%10
    no_of_digits=no_of_digits+1
    number=number//10           #number of digits are calculated here    
print("number of digits of","\"",temp,"\":",no_of_digits)
sum=0
temp2=temp
while temp2>0:               # use another copy
   digit=temp2%10
   sum=sum+(digit**no_of_digits)
   temp2=temp2//10
print("sum of digits of","\"",temp,"\":",sum)
if sum==temp:
    print("----",temp,"is Armstrong number----")
else:
    print("----",temp,"is not Armstrong----")
```
## Qn43: *Perform following operations on given list*
- Access Elements: Print the third element.
- List Length: Print the number of elements in the list
- Check if Empty: Write a code to check is list empty.
` given list=[10, 30, 50, 70, 90, 0]`
### solution:
``` python
given_list=[10,30,50,70,90,0]
#first operation:
print(given_list[2],"is the third element")


#second operation:
print("no.of elements:",len(given_list))


#third operation:
lenght_of_list=len(given_list)
if length_of_list==0:
    print("The given list is empty")
else:
    print("The given list is non empty")
```
## Qn44: *Perform following list manipulation operations on given list:*
` list=[10, 20, 30, 40, 50, 60, 70]`
- Change Element: Change the second element of a list to 200 and print the updated list.
- Append Element: Add 600 o the end of a list and print the new list.
- Insert Element: Insert 300 at the third position (index 2) of a list and print the result.
- Remove Element (by value): Remove 600 from the list and print the list.
- Remove Element (by index): Remove the element at index 0 from the list print the list.
### solution:
```python
list=[10, 20, 30, 40, 50, 60, 70]
print("Initial list",list)
list[1]=200  
   # this changes the second element to 200, remember the index value of an 'n'th element is (n-1).
print("List after changing second element",list)


list.append(600)     
   #append() function always add the element on to the last position of the list
print("list after adding 600 on last postion",list)


list.insert(2,300)
   #syntax: list_name.insert(index,element) ,implies adds the given element in the given index postion
print("list after adding 300 in third position",list)


list.remove(600)
     #Always remember remove() function removes the first occurance of the given value from the list
print("list after removing first occurance of 600",list)

del list[0]
print("list after removing element at index 0:",list)
```
## Qn45 *Calculate and print the sum and average of all numbers in a given list*
`list=[10,20,30,40,50]`
### solution:
```python
list=[10, 20, 30, 40, 50]

sum=0
for element in list:
    sum=sum+element
print("sum of elements:",sum)

no_of_elements=len(list)
avg=sum/no_of_elements
print("average of elements of the list:",avg)
```
## Qn46: *Create a copy of a list [10, 20, 30] and modify the copy. Print both the original and the copied lists to demonstrate they are independent.*
### solution:

```python
original_list=[10, 20, 30]
print("Original list",original_list)

first_copy_list=original_list[:]
print("first copy of original list:",first_copy_list)
first_copy_list.append(40)
print("modified first copy of original list:",first_copy_list)

second_copy_list=list(original_list)
print("second copy of original list:",second_copy_list)
second_copy_list.append(90)
print("modified second copy of original list:",second_copy_list)

third_copy_list=original_list.copy()
print("third copy of original list:",third_copy_list)
third_copy_list.append(80)
print("modified third copy of original list:",third_copy_list)

#List slicing ([:]) is used to create a shallow copy. It creates a new list containing all the elements of the original list, so copied_list is a distinct object in memory from the original_list.

#another_copy = list(original_list): This uses the list() constructor to create a new list from an existing one, also resulting in a shallow copy.

#third_copy = original_list.copy(): This is the most direct way to create a shallow copy, available from Python 3.3 and onwards
```
## Qn47 *Remove an empty string from a list of strings*
``` given_list=["mk", " ", "MK", "msmk"]```
### solution:
``` python
given_list=["elephent",0, "MK",None,False, "thengakkola"]
print("Given list: ",given_list)
updated_list=list(filter(None,given_list))
print("updated list",updated_list)
#filter(function, iterable)

#filter() keeps only those elements for which function(element) is True.
#Why None is used?
#If the function is None, Python automatically uses bool() on each element.
#So it keeps elements whose bool(value) is True.
#What are falsy values?
#These evaluate to False in Python:

"""
- 0

- 0.0

- '' (empty string)

- None

- False

- [], {}, ()
"""
```
## Qn48 *Write a python program to  







