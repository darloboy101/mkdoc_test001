# Displaying code and mathematical syntax

This page highlights some of the options for how code samples and more complicated mathematical content could be displayed.

## Static code

Here are some code blocks that illustrate the options available in MkDocs with the Material theme and the Pygments and CodeHilite plugins. Note that code samples have a built in copy function, which may be useful.


### 1. Code without line numbers

``` python
""" Bubble sort """
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

### 2. Code with line numbers

``` python linenums="1"
""" Bubble sort """
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

### 3. Code with line numbers and highlighted lines

``` python linenums="1" hl_lines="3 4"
""" Bubble sort """
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

### 4. Inline code samples

Here is some text where the code is displayed inline with language-specific highlighting: `#!py3 import pymdownx; pymdownx.__version__`. The next sentence then continues.

The mock shebang will be treated like text here: ` #!js var test = 0; `.


### 5. Tabbed code 

Tabbed blocks can contain any standard markdown content, but can be particularly useful for code. 

Here they've been used for a sequence. But they they could be used to show the same code in different languages; to show variant approaches; etc.

=== "Step 1"

	Here is some explanatory text.

	``` python
	""" Bubble sort """
	def bubble_sort(items):
	```

=== "Step 2"
	Here is some more explanatory text.

	``` python
	""" Bubble sort """
	def bubble_sort(items):
	    for i in range(len(items)):
	```

=== "Step 3"
	``` python
	""" Bubble sort """
	def bubble_sort(items):
	    for i in range(len(items)):
	        for j in range(len(items) - 1 - i):
	```

=== "Step 4"
	``` python
	""" Bubble sort """
	def bubble_sort(items):
	    for i in range(len(items)):
	        for j in range(len(items) - 1 - i):
	            if items[j] > items[j + 1]:
	```

=== "Step 5"
	``` python
	""" Bubble sort """
	def bubble_sort(items):
	    for i in range(len(items)):
	        for j in range(len(items) - 1 - i):
	            if items[j] > items[j + 1]:
	            items[j], items[j + 1] = items[j + 1], items[j]

	```



## Mathematical syntax

MkDocs with the Material theme uses the [Arithmatex](https://facelessuser.github.io/pymdown-extensions/extensions/arithmatex/) plugin to add MathJax support in markdown.

### 1. Using MathJax in a block 

$$
\frac{n!}{k!(n-k)!} = \binom{n}{k}
$$

<hr>

$$
E(\mathbf{v}, \mathbf{h}) = -\sum_{i,j}w_{ij}v_i h_j - \sum_i b_i v_i - \sum_j c_j h_j
$$

<hr>

\[3 < 4\]

<hr>

\begin{align}
    p(v_i=1|\mathbf{h}) & = \sigma\left(\sum_j w_{ij}h_j + b_i\right) \\
    p(h_j=1|\mathbf{v}) & = \sigma\left(\sum_i w_{ij}v_i + c_j\right)
\end{align}


### 2. Using MathJax in-line.

Lorem ipsum dolor sit amet: $p(x|y) = \frac{p(y|x)p(x)}{p(y)}$

Lorem ipsum dolor sit amet: $E(\mathbf{v}, \mathbf{h}) = -\sum_{i,j}w_{ij}v_i h_j - \sum_i b_i v_i - \sum_j c_j h_j$


## Executable and editable code samples

We need to establish whether it is a requirement to include editable and executable code samples in the online lessons.

Jupyter notebooks can be added as pages to a MkDocs project -- however, the output will be rendered as static content and will not be editable / executable by the end user.

If any code samples do need to be editable / executable, they will need to be embedded from an external service. That could include services that are freely available; services to which we set-up a license/subscription; or a service the University itself hosts.  

### 1. Embedding code samples from Trinket

Trinket is an established site that has focussed particularly on education uses.

#### Simple example

<iframe src="https://trinket.io/embed/python3/04f5c0691b" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

#### More complex example

<iframe src="https://trinket.io/embed/python/65e6386f72" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


### 2. Embedding code samples from repl.it

Another site that offers embeddable code options.

<iframe height="400px" width="100%" src="https://repl.it/repls/BrownIntentionalLevels?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

