# Strings, list and indices

In this section you will explore some basic operations and typical uses of code such as going through a list of words to separate into types of words. 

These are algorithmic elements from which more complicated procedures can be defined. Code will be embedded throughout the lesson to exemplify. 

!!! info "Learning outcomes"
	By the end of this lesson you will:

	* [x] understand how to extract individual letters from a string, using an *index* giving the position of the letter,
	* [x] be able to *slice* strings to extract sub-strings,
	* [x] know how to use the `#!py3 split()` method to divide a string up into a
	sequence of sub-strings.


## 1. Extracting individal letters from a string

### 1.1 Indexing a Character of a String

A character can be extracted from a string by means of an index number in square bracket after the string:

``` bash 
	>>> "hello"[1] 
	'e'
	>>> "hello"[0] 
	'h'
	>>> "hello"[4]
	'o'
	>>> "hello"[5]
	Traceback (most recent call last):
  		File "<pyshell#56>", line 1, in <module>
    	"hello"[5]
	IndexError: string index out of range		
```

### 1.2 Using a Variable as an Index

It is rarely useful to extract a character from a particular string by directly specifying a numerical index. In this case we may as well just put the character itself in our code (e.g. `#!py3 "hello"[1]` is always the character `#!py3 'e'`).

In most cases the index will be a variable (it could also be a mathematical expression):


``` python linenums="1"
test_string = "This is a test string."
for i in range( len(test_string) ):
    print( test_string[i] )

```

### 1.3 Negative String Indices

If you use a negative number `#!py3 -n` as an index, this refers to the character obtained by counting `#!py3 n` characters back from the end of the string:


``` bash
>>> "this is a string"[-6] 
's'
>>> "this is a string"[-1] 
'g'
>>> "this is a string"[-0] 
's'

```

Note that `[-1]` gives you the last character of the string, whereas `[-0]` is the same as `[0]` (since `[-0]` is not really negative).


## 2. Slicing strings 

### 2.1 Extracting a Slice of a String

You can also extract a sub-string (slice) of a string by specifying a range of indices using the `:` character:

``` python
>>> "hello everyone"[6:11] 
'every'
```

Slicing is useful when you have information stored in formatted strings and want to extract parts of it.

For example:

``` python
booking_spec = "18.10.2013--21.10.2013 --- Class: std"
booking_end_date = booking_spec[12:22]
```

### 2.2 Slicing with Negative Indices

The slicing notation also works with negative indices:

``` python
>>> s = "The second to last word is" 
>>> s.[-7:-3]
'word'
```

### 2.3 The Empty Slice

If the first index of a slice specification is equal to or higher than the second index.

``` python
>>> "hello everyone"[6:4] 
''
```

But if either of the two indices were outside the range of indices that lie within the string you would get an error.

### 2.4 Slicing from the Beginning or End

If you omit an index, before or after the `:` in a slice specifier, Python uses the index corresponding to the beginning or end of the string.

This is particularly useful when you don’t know how long the string is:

``` python
>>> s = "abcdefghijklmnop" 
>>> s[-5:]
'lmnop'
```

What is the value of the following expression:

``` python
"What’s going on?"[:]
```

## 3. The Split method

### 3.1 Splitting Up a String

You may want to divide up a string into a sequence of parts. This can be done using the `.split()` method.

``` python
>>> "This sentence contains: five words.".split() 
['This', 'sentence', 'contains:', 'five', 'words.']
```

Note that the result is a *list*  data structure. (More on these next lecture.)

In a program we might have:

``` python
	for word in wordstring.split():
    	print( word ) 
```

### 3.2 Splitting on other Separators

When using the simple `.split()` method, the string is split up wherever one or more *whitespace* characters occur (spaces, tabs, newlines).

But, we can actually specify any string to be used to find the splitting points:

``` python
>>> "this--that--and--the-other".split(r'--') 
['this', 'that', 'and', 'the-other']
```

## Conclusion 

- Python provides a very versatile range of operations that can be performed on lists.

- Individual characters and ranges of characters (called sub-strings or slices) can be extracted using a fairly simple but flexible notation.

- The `.split()` method gives a high-level way of going from a string to a *list* of its constituents, which are divided up by identifying separating substrings (typically spaces).