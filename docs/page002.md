# Tuples and Lists

In this section you will explore lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam. 


!!! info "Learning outcomes"
	By the end of this lesson you will:

	* [x] understand the basic ideas and uses of tuples and lists
	* [x] appreciate the difference between tuples and lists
	* [x] understand the most significant operations that can be applied to lists.
	* [x] get a feel for the kinds of program functionality that are supported by lists and tuples.


## 1. Introduction to Tuples and Lists

### 1.1 What are Tuples and Lists?

Lists and tuples represent sequences of data. For instance, we may have a list of numbers, letters, or words. We can even have several types of object in a single list.

Python uses round brackets to represent a tuple and square brackets to signify a list:

``` python linenums="1"
myTuple = (1, 2, 3)
myList = [1, 2, 3]		
```

!!! Question
    What would happen if you put `#!py3 myList = (1, 2, 3)` ?
	
	??? "Answer"
		Lorem ipsum.

### 1.2 Why have both tuples and lists?

Although tuples and lists both represent sequences of data items, they have different computational properties.

- Tuples take up less memory and can be accessed faster than lists.

- Lists can be manipulated much more flexibly than tuples. 

Tuples also play a special role in representing the parameters that
are passed to and returned from procedures/functions.


### 1.3 Tuples vs Lists

The fundamental difference is that you can change a list but a
tuple always stays the same.


``` bash
>>> myList[1] = 666
>>> myList
[1, 666, 3]

>>> myTuple[1] = 666
Traceback (most recent call last):
  File "<pyshell#181>", line 1, in <module>
    myTuple[1] = 666
TypeError: 'tuple' object does not support item assignment

```


### 1.4 List Examples

Lists (and tuples) can take a huge variety of forms:

``` python linenums="1"
list_of_numbers = [1, 3, 7, 9, 12, 10, 2]

list_of_strings = ["this", "is", "a", "list"]

nested_list = [ [1,2,3], [4,5,6], [7,8,9] ]

character = [ "Bob", 27,
              ["items", ["gun", "cake", "onion"]]
            ]
```

Note that you can break lines within brackets (either square or round) without Python complaining about bad indentation. 

This can be useful for laying out complex data in lists so that it is easy to read.



## 2. Working with Lists and Tuples

### 2.1 Looping over Lists and Tuples

You can use the `for` keyword to loop over either tuples or lists and do useful things with their elements:

``` python linenums="1"
numbers = (1,4,6,7,3,2)
   for num in numbers:
       if num > 3
          print num
```

### 2.2 Concatenating (Joining) Lists

When applied to lists, the ‘+’ operator, joins them together to create a new list:

``` python
>>> [1,2,3,4,5] + [6,7,8,9,10]
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

We can use this to accumulate values in a list:

``` python linenums="1"
def makeCubeList( n ) :
    cubelist = []         # start with empty list
    for n in range( n+1 ):
        cubelist = [n**3] + cubelist
    return cubelist
```

### 2.3 List Slicing

To extract parts of a list, you can use exactly the same slicing operators that can be applied to strings.

Suppose we have: `#!py3 mylist = [’a’, ’b’, ’c’, ’d’, ’e’, ’f’, ’g’]`

What is the value of:

- `#!py3 mylist[2:7]` 
- `#!py3 mylist[4:]`
- `#!py3 mylist[-2:]` 
- `#!py3 mylist[1:-1]`

??? "Answer"
	- Lorem ipsum.
	- Lorem ipsum.
	- Lorem ipsum.
	- Lorem ipsum.


### 2.4 The Append Method

Lists are *objects* and thus can be manipulated using certain pre- defined *methods*:

``` python
>>> a = [1,2,3]
>>> a.append(4)
>>> a
[1, 2, 3, 4]
```

### 2.5 Reversing a List

As one might expect, the reverse method reverses the elements of a list:

``` python
>>> a = [1,2,3,4]
>>> a.reverse()
>>> a
[4, 3, 2, 1]
```

However, perhaps unexpectedly, the reverse method does not actually return the reversed list as a value:

``` python
>>> a = [1,2,3,4].reverse()
>>> print(a)
None
```

(Assigning a variable to an expression that does not return a value gives it the value None.)


### 2.6 Deleting Elements from a List

The del operator can be used to delete elements or slices from a list:

``` python
>>> mylist = ['a', 'b', 'c', 'd', 'e', 'f', 'g'] >>> del mylist[3:6]
>>> mylist
['a', 'b', 'c', 'g']
```

### 2.6 Typical Coding Examples

!!! Example "Find the common element in two lists"
	``` python linenums="1"
	def commonElements( listA, listB ):
	    common = []
	    for a in listA:
	        for b in listB:
	            if a == b:
	               common = common + [a]
	               break
	    return common
	```

### 2.7 List Comprehension


The idea of list comprehension is quite advanced. You probably won’t use it for a while but it is useful to be aware of it.

We can create a list by directly specifying how to generate its successive values from the range of a for loop:

``` python
>>> [ x**2 for x in range(10)]
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

We can even apply a further filter to only add certain generated elements to the list

``` python
>>> [ x**2 for x in range(10) if x*x % 2 == 0]
[0, 4, 16, 36, 64]
```

## List questions

!!! Question
    What will get printed by the following?
    	``` python
		list = ['w', 'o', 'r', 'k'] del list[0]
		del list[2]
		print( list )
		```
	
	??? "Answer"
		Lorem ipsum.


!!! Question
	What is the value of each of the following:

	- `#!py3 [’a’, ’b’] * 3+[5]`
	- `#!py3 [’a’, ’b’, ’c’, ’d’, ’e’][0:2] + [’x’,’y’,’z’][-2:]` 
	- `#!py3 [x for x in [1,3,4,3,6,2] if x > 2]`
	
	??? "Answer"
		Lorem ipsum.


## Conclusions

- *Lists* provide a very powerful and flexible data structure that supports many computational techniques for high-level information processing.

- It will probably take a while for you to realise the full potential of lists. You should experiment with some of the basic features rather than try to understand everything at once.

- *Tuples* provide the same basic data structuring capabilities as lists but cannot be altered so do not provide so much functionality.

- But tuples require less memory and are more efficiently processed.

