# Introduction to Python

On this page we have rebuilt a section of existing content from [Programming for the Web](https://soc-dm.leeds.ac.uk/module/40/view) as a proof of content.

**Learning outcomes:**

By the end of this unit you will:

* [ ] Aenean pretium efficitur erat, donec pharetra, ligula non scelerisque
* [ ] Nulla vel eros venenatis, imperdiet enim id, faucibus nisi
* [ ] Praesent sed risus massa


## An overview

Lorem

<div class="video-wrapper">
  <iframe scrolling="auto" marginheight="0" marginwidth="0" src="//mymedia.leeds.ac.uk/Mediasite/Play/21d593b9c4f44074a14fceed4726d7eb1d" width="100%" height="400" frameborder="0"></iframe>
</div>

- [Link to transcript]()
- [Link to slides]()


##  What is programming? 

Before we describe what programming is first it is essential that we understand what a computer is and what a computer does. A computer is a machine that computes, it may be a person who manually computes values or it may be some electromechanical device. Most people will be familiar with digital computers, the type you are most likely reading this content on. All computers have a single task, that is to compute some value. How the computer computes such a value is the responsibility of a computer programmer.

A computer program can be thought of as a set of instructions, which will lead the computer to calculating the correct value. In the context of a human computer, this may be a set of instructions written in English, like a recipe for baking a cake. However, English is an ambiguous language, allowing a sentence to be interpreted in many different ways. This ambiguity can have disastrous consequences. A computer programming language is an unambiguous language which allows the programmer to communicate a set of instructions to a computer.

At the advent of the modern digital computer, the method of provide instructions to the computer was very primitive. Each instruction carried out a single operation and many instructions were needed to do simple operation such as adding two numbers together. These types of programming language are called low level language, they provide a very thin layer of abstraction from the physical device a computer program is running on and require an in depth knowledge of the computers architecture. In this module we will be learning a high level programming language. High level programming languages provide a high level of abstraction away from the physical computer that is carrying out the instructions. These types of programming languages have constructs such as `variable` , `for` loops and `if` statements (we will be introducing these topic this week).

In this module we will be using the Python programming language. The Python programming language first appeared in 1991 and was designed by Guido van Rossum. Python is a multi-paradigm programming language incorporating many features which are also found in many other modern programming languages, such as [object orientation](https://en.wikipedia.org/wiki/Object-oriented_programming), [functional programming](https://en.wikipedia.org/wiki/Functional_programming) and [meta programming](https://en.wikipedia.org/wiki/Metaprogramming). Python differs from some modern programming languages by the fact that it is an interpreted language, we will learn more about what this means later. Python is one of the [top ten](https://www.tiobe.com/index.php/content/paperinfo/tpci/index.html) most used programming languages (as of May 2015). Because of these reasons, Python is among the best programming languages to learn for a first language for people outside the field of computer science, it will allow us to introduce programming concepts which will be transferable to many other modern computer languages while allowing us to avoid some of the awkwardness of some other languages.

In addition to the Python programming language we will also use javascript. Javascript is a very common programming language which is used by web developers to create interactive and user friendly webpages. We will transfer the knowledge and understanding of programming, that you will have developed while learning Python, into the context of programming Javascript. Both Python and Javascript form the foundation of modern web programming.


##  What can you expect?

In this module you can expect to learn the fundamental concepts of programming, you will gain the experience to apply these concepts to programming in Python and Javascript. This module will start you on a long road to becoming a competent software developer.

Each week you will be presented with a set of new topics to learn. These topics will be presented in an interactive way; we will present the theory, provide examples, discuss the advantages and disadvantages of different approaches and finally there will be exercises. Although the exercises are not directly accessed, they will be essential for you to develop the skills required to complete the multiple choice questions on the vle and the courseworks.

The module will be assessed via three pieces of coursework which are available for you to browse now on the module homepage. You may hand them in at any time up to the submission deadline. The pace at which you progress through the content is your choice, we have broken the content into blocks that we believe are achievable in six hours each (equivalent to one weeks work).

The module is supported via lab classes which are your opportunity to ask question to the module staff and to get feedback on your solutions to exercises. The times and locations of the lab classes can be found on the module homepage.

The table below outlines the topics that wil be covered during this module and in which week they are introduced.

| Week | Data type | Key words | Operations | Programming topics | Application topics |
| ------------ | ------------- | ------------ | ------------ | ------------- | ------------ |
| 1 | Numeric, Strings and Booleans | `if`/`else`, `for` and `range` | `+`, `*`, `-`, `/` | Indentation | Hello world, using loops and conditionals |
| 2 | Lists and Decimals  | `while`, `elif` | `%`, `!`, `and`, `or` | | |
| 3 |   | `break`, `continue` | `%`, `!`, `and`, `or`  | | |
| 4 | tuple  | `def`, `return` | `%`, `!`, `and`, `or` |  | |
| 5 |   | `try`, `except` | | File I/O | |
| 6 | Dictionaries | | |  | |
| 7 |  | `import`| | Using libraries | |
| 8 | | | | | |
| 9 | Objects | `class` | | | |
| 10 | Strings, Numerics, List and Functions | | `+,*,-,/`| JavaScript Syntax | |
| 11 |  |  | | HTML DOM	| |
| 12 |  |  | | External APIs | |


## Getting started with Python

In this module we will be using Python version 3. In 2008 Python 3 was released which is not compatible with earlier versions of Python.

!!! warning
    A cautionary note, if you search for additional resources in books or online make sure that any articles you read are for Python 3.

All university cluster machine have Python 3 installed as well as Spyder 3 (a program that we will be using later), therefore you will not need to install Python 3 or Spyder. However, if you wish to complete this course on your own computer you will need to make sure you have the correct software installed. All of the software you will need to complete this course is free and open source.

### Installation

In order to be able to run Python programs on your own computer you will need to make sure you have Python installed. To check if you have Python installed open up a terminal and type `python --version` followed by an enter. If you get an output such as 'Python 3.x.y' where x,y are numbers then you have Python 3 installed correctly and you may skip to the next sections. If you get any other message then continue reading the installation instructions relevant to your operating system below.

We have found that the most straightforward way of installing Python 3 and Spyder is to use the Anaconda installation. This can be found [here](https://www.continuum.io/downloads).

Follow the instructions to get the version suitable for you operating system. Make sure you get the Anaconda 3.4 version.

If the Anaconda version does not work for some reason, you could try one of the following alternatives:

#### Windows

To install Python on a Windows machine go to the Python website and download the appropriate Windows installer ([x86](https://www.python.org/ftp/python/3.4.3/python-3.4.3.msi)/ [x86-64](https://www.python.org/ftp/python/3.4.3/python-3.4.3.amd64.msi)). To start the installation process, navigate to the folder you saved the installer file into and double click on the file. You should accept all default values that the installer provides.

To ensure that the installation has been successful open up a terminal and type `python --version`. You should now see a meesage such as 'Python 3.4.3'.

#### Mac

To install Python on a Mac machine go to the Python website and download the appropriate Mac installer (64-bit/32-bit/ i386/PPC). To start the installation process, navigate to the folder you saved the installer file into and double click on the file. You should accept all default values that the installer provides.

To ensure that the installation has been successful open up a terminal and type `python --version`. You should now see a meesage such as 'Python 3.4.3'.

#### Linux

To install Python on a linux distribution, please refer to the help pages of your specific distribution. Links to some of the more popular distributions are provided below.

**Distribution**  | **Installing Python 3**
------------- | -------------
Ubuntu | Installed by default
Debian | Installed by default
Fedora | Installed by default
Gentoo | Installed by default
Arch | `pacman -Sy python`

### Introducing the interactive mode

The Python programming language is an interpreted language and therefore your code does not need compiling like some other languages (e.g. C/C++, Java, .net). Because of this it is possible to interact with the Python interpreter interactively, that is, you type an instruction and it will process it and give you a response if one is due. As an introduction to the Python programming language we will explore the interactive Python interpreter before continuing. 

Open a terminal and start a Python interpreter by typing `python`. You should see text similar to the following.

``` 
Python 3.2.2 (default, Sep 26 2011, 17:16:37) 
[GCC 4.4.4 20100726 (Red Hat 4.4.4-13)] on linux2
Type "help", "copyright", "credits" or "license" for more information.
>>> 
```

The three angled brackets ( `>>>` ) denote the Python prompt and you can type instructions for the Python interpreter to execute. During this module you will be presented with exercise, some of which can be completed using a Python interpreter which is embedded in the webpage. By using the interpreter embedded in the webpage you will be able to try out snippets of code (a small piece of code) when you are working on a computer that does not have Python installed. Where it is possible to use an embedded interpetter you will see a button labelled 'Try it yourself'.

Let us explore the Python interpreter. Open a terminal and open the Python interpreter (you should now see the Python prompt). Into the Python interpreter type the follow.

``` python
print("Hello World!!!")
```
Once you press eneter you will see something similar to

``` 
Python 3.2.2 (default, Sep 26 2011, 17:16:37) 
[GCC 4.4.4 20100726 (Red Hat 4.4.4-13)] on linux2
Type "help", "copyright", "credits" or "license" for more information.
>>> print("Hello World!!!")
Hello World!!!
>>>
```

You have successfully written your first program in Python. Throughout this module you will see snippets of code, they are formatted to standout from the surrounding text. Each time you encounter a snippet of code you should carefully read it and understand what each line does. Each snippet of code will be accompanied with a brief explanation of what it does.

The Python interpreter can act like a calculator, try running the following instructions.

``` python
2 + 2
```
The symbol `+` is the symbol that denotes addition of numbers in Python.

``` python
3 * 3
```
The symbol `*` is the symbol that denotes multiplication of numbers in Python.

``` python
2 + 4 * 5
```
In Python the evaluation of mathematical expressions is identical to that in mathematics. It is possible to alter the evaluation order by using round brackets.

``` python
(2 + 4) * 5
```

!!! info 
    Python is whitespace dependent. Whitespace is any character that alters the formmating of text but does not display a printed character, such as spaces, tabs and new lines. Whitespace symbols in Python have meaning, so when you are writing your programs in this module take care to ensure you have no extra whitespace characters.

### Integrated development environments

Although the interactive Python interpreter is useful, when it comes to writing programs that you want to keep it is awkward as you can not save the sequence of instructions you have just enetered. We would like a method of saving a sequences of instructions so that we can execute them whenever we wish. Files that contain Python instructions, sometimes called Python code, are suffixed with the file extenion `.py`. 

It is possible to write Python code in any text editor, however, there is a more convenient way. An integrated development environment (IDE) is a program that makes developing programs easier. IDE's often contain useful tools like automatic formatting, colour coding and tools to help you figure out why a program is not behaviouring as you expect. The IDE that will be used in this module is called Spyder and is a cross platform IDE. Spyder is not included in the standard Python installation so we must install it separately (Spyder is installed by default on the university machines).

#### Installing Spyder

To install Spyder download the appropriate installation file for your operating system.

Operating system | Download
------------- | -------------
Windows | [32-bit](https://bitbucket.org/spyder-ide/spyderlib/downloads/spyder-2.3.4.win32-py3.4.exe)/[amd-64](https://bitbucket.org/spyder-ide/spyderlib/downloads/spyder-2.3.4.win-amd64-py3.4.exe)
Mac | [Spyder](https://bitbucket.org/spyder-ide/spyderlib/downloads/spyder-2.3.4-py2.7.dmg)
Linux | [Spyder](https://bitbucket.org/spyder-ide/spyderlib/downloads/spyder-2.3.4.zip)


#### Introduction to Spyder

Lorem ipsum.

<div class="video-wrapper">
  <iframe scrolling="auto" marginheight="0" marginwidth="0" src="//mymedia.leeds.ac.uk/Mediasite/Play/dcc861d2ef4540b097b351963d245bb21d" width="100%" height="400" frameborder="0"></iframe>
</div>

- [Link to transcript]()

#### Experimenting using Spyder 

A further look at Spyder's interactive console.

<div class="video-wrapper">
  <iframe scrolling="auto" marginheight="0" marginwidth="0" src="//mymedia.leeds.ac.uk/Mediasite/Play/32ec770a0b984e809ab8b057869b6f911d" width="100%" height="400" frameborder="0"></iframe>
</div>

- [Link to transcript]()


## First program

We will now write our first program using Spyder, this will allow us to save the program so that we can run it again later is we wish. This will also allow us to change and reuse our code. To create and run a program in Spyder, carry out the following steps:

- Open the Spyder application

- Click on File > New File, this will create a new editing tab.

- Inside the editing tab type the following:

``` python
print("Hello from Spyder IDE")
```

- Save the file by clicking, File > Save(select an appropriate folder and filename)

- Run your program by clicking Run > Run (alternative the shortcut F5 will run the current file)

Throughout this workbook there are many exercises to complete and most of the exercises require you to write programs. It is essential that you give your programs sensible filenames so that you can come back to them later. A recommendation is that you create a new file for each exercise that your attempt, this will suffice until you start developing larger programs later in the module.


### A simple example

Using the same steps as before will we create a new file in Spyder to create another example. A program can seem a little useless if it does not interact with the user, in the next section we will cover how to get the program to prompt the user for input. Create a new file in Spyder, the same way as you did in the previous task and type the following code. Once you have typed in the code run the program and see what the application does.

``` python linenums="1"
## Program for computing and displaying squares of numbers
print("***********************************************")
print("Welcome to the Amazing Square Computing Program")
print("Enter any whole number :", end ="")
 
# Reads in a string of characters
numstring = input()
 
# Converts the string to a whole number
number = int(numstring)
 
# Prints a string to the shell
print ("The square of" , number , "is" , number * number , " !!! ")
```

This simple program prompts the user to enter a whole numer (line 4-7), the value that the user enters is then converted into a number (line 10) and then the program will print out a message reporting the number that the user entered followed by the square of the number. The process of converting the users input to a number if a topic we will explore in detail later.

### Your turn

Try the following questions, you may find it useful to keep a written note of your answers for when it comes to completing the coursework.

!!! Question "Question 1"
    What is the result of the following instructions?
    
    ``` python
    7 / 4		
    ``` 
	
	??? note "Sample solution"

	    ``` python
	    1.75	
	    ```

!!! Question "Question 2"
    What is the result of the following instructions?
    
    ``` python
    2 ** 2		
    ``` 
	
	??? note "Sample solution"

	    ``` python
	    4	
	    ```

!!! Question "Question 3"
    What is the result of the following instructions?
    
    ``` python
    name = "Snake master"		
    ``` 
	
	??? note "Sample solution"
		The result is this instruction is to assign a variable named `name` the value "Snake master".

!!! Question "Question 4"
    What is the result of the following instructions?
    
    ``` python
    for x in range(5):
	print("Python is the best")		
    ``` 
	
	??? note "Sample solution"
		The code prints out: 
		``` python
	    Python is the best
		Python is the best
		Python is the best
		Python is the best
		Python is the best	
	    ```

!!! Question "Question 5"
    Try to determine what the symbol `%` does in Python. Try entering the following instruction replacing the numbers by a few different values
    
    ``` python
    7 % 4	
    ``` 
	
	??? note "Sample solution"
		The % symbol is the modulus symbol, it will return the remainder when the first number is divided by the second number.

!!! Question "Question 6"
    Write a program that prints out your name in ascii art, similar to the example below.
    
    ``` python
    print(" CCC  OOO  M   M PPPP   11  0000 0000   11 ")
	print("C    O   O MM MM P  P  111  0  0 0  0  111 ")
	print("C    O   O M M M PPPP   11  0  0 0  0   11 ")
	print("C    O   O M   M P      11  0  0 0  0   11 ")
	print(" CCC  OOO  M   M P     1111 0000 0000  1111")	
    ``` 


## Unit review

* [x] Aenean pretium efficitur erat, donec pharetra, ligula non scelerisque
* [x] Nulla vel eros venenatis, imperdiet enim id, faucibus nisi
* [x] Praesent sed risus massa
