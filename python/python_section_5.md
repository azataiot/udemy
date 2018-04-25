# Python Section 5 
## 32. if ,else if ,end   
* if  
``` python 
if some_condition:
#excudte some code
```  
``` python  
if hungry:
    print('feed me !')
else:
    print('I am not hungry!')
```
* elif
``` python  
Ioc =   'Bank'

if Loc  ==  'Auto Shop':
    print('Cars are cool!')
elif Loc    ==  'Store':
    print('sssss')
else:
    print('sssss')
```    
* else

## 34. For loops in Python   (*iterable*)
string : NOT iterable  
list : IS iterable   

Syntax of a for loop:
``` python
my_iterable =   [1,2,2] 
for item_name in my_iterable:
    print(item_name)
``` 

## 35. While Loops in Python  
Syntax of a while loop :  
``` python  
while some_boolean_condition:
#do something
```  
or :
``` python 
while some_boolean_condition:
    #do something
else:
    #do some differrent thing
```  

We can use break ,continue, and pass statements in our loops to add additional functionality for various cases. The three statements and defined by:   
* break
definition: Breaks out of the current closest enclosing loop.
* continue
definition: Goes to he top of the closest enclosing loop.  
* pass
definition: Dose notiong at all.

Examples: 
``` python 
x   =   [1,2,3]
for item in x:
    #comment
    pass

print('nothing happend')
``` 
continue:
``` python  
my_string   = 'Sammy'
for letters in my_string:
if letter   ==  'a':
    continue
print(letter)
```  
result:  
`s `  
`m `  
`m`   
`y`   

break:  

``` python  
my_string   = 'Sammy'
for letters in my_string:
if letter   ==  'a':
    break
print(letter)
```  
result: 
`s`     

## 36. Useful Operators in Python 
* `range()`   
``` python
for num in rang(10):
print(num)
```   
* range(0,10)   
``` python
for num in rang(1,10):
print(num)
```   
* range(0,11,2)   
``` python
for num in rang(1,11,2):
print(num)
```   

* `index count`

``` python 
index_count =   0
for letter in 'abcde':
    print('At index {} the letter is {}'.format(index_count,letter))
    index_count +=  1
```

results:    
At index 0 the letter is a   
At index 1 the letter is b  
At index 2 the letter is c  
At index 3 the letter is d  
At index 4 the letter is e      


``` python 
index_count =   0
word    =   'abcde'
for letter in word:
    print(word[index_count])
    index_count +=  1
```

* `enumerate()`
``` python 
word    =   'abcde'
for index,letter in enumerate(word):
    print(index)
    print(letter)
    print('\n')
``` 
results:    
0   
a   

1   
b   


....    
* `zip()` function  
``` python  
mylist1 =[1,2,3]    
mylist2 =['a','b','c']  
for item in zip(mylist1,mylist2):
    print(item)
```   

results:    
``` python 
(1,'a')
(2,'b') 
(3,'c')
```     
### another example of zip :
``` python  
mylist1 =[1,2,3]    
mylist2 =['a','b','c']  
mylist3 =[100,200,300]
for item in zip(mylist1,mylist2,mylist3):
    print(item)
```   

results:    
``` python 
(1,'a',100)
(2,'b',200) 
(3,'c',300)
```     
for interest: what happens if elemts are not the same ?

``` python  
mylist1 =[1,2,3,4,5,6]    
mylist2 =['a','b','c']  
mylist3 =[100,200,300]
for item in zip(mylist1,mylist2,mylist3):
    print(item)
```   

`results: `   
``` python 
(1,'a',100)
(2,'b',200) 
(3,'c',300)
```     

* in operator   
``` python 
'x' in  ['x','y','z']
#results : returns: `True`
``` 
**This is a very quick way to check is there something in the list**
* in operator   
``` python 
'x' in  'a world'
#results : returns: `True`
```     
``` python 
'mykey' in  {'mykey':'1234'}
#results : returns: `True`
```     
``` python  
d   =   {'mykey':'1234'}
1234 in d.values()
#results : returns: `True`
```     

``` python  
d   =   {'mykey':'1234'}
1234 in d.keys()
#results : returns: `False`
```     

* Some mathimatical functions here  
``` python 
mylist  =   [10,20,30,40,100]   
min(mylist) 
max(mylist) 
```


* `import` function   
``` python  
from random import shuffle  
mylist=[1,2,3,4,5,6,7,8,9,10]
shuffle(mylist)
print(mylist)
#results: [3,9,7,8,10,5,1,2,6,4]
```     

`randint` function  : random integer 

``` python 
randint(0,100)
# result: 79
```     
``` python  
mynnum=randint(0,10)
print(mynum)
#result 3
``` 
`input` function 
``` python 
input('Enter a number here : ')
Enter a number here:    50
'50'
``` 

**!!!! input()always accept the input as a *string***

get an integer in input 
``` python  
result  =   int(input('input your favoroute number plz:'))

input your favoroute number plz:    30
result  =   30
```  






