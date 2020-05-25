# Welcome

We're considering using [MkDocs](https://www.mkdocs.org) with the [Material theme](https://squidfunk.github.io/mkdocs-material/) as the basis for displaying some of the content within the distance learning AI module. 

Some of the advantages we've identified are:

- MkDocs is Python based and can be installed using Pip. Docker images for Mkdocs with material are available. As such, should be convenient for DES and Computer Science to use.

- Material theme is adaptable and provides a high standard of accessibility and mobile usability out of the box.

- Content will be processed to a static site that can be hosted from the Minerva content collection. This will significantly simplify requirements for the hosting / maintenance of content. 

- International students with bandwith challenges should be able to download content to view locally. It should be possible to process MkDocs content to additional formats, such as PDF and ePub. 

- Robust support for displaying Python code samples using Pygments and CodeHilite.

- Content can be authored in Markdown. Integration with git may further facilitate workflow.

- Admonition extension allows block-styled content that supports pedagogical uses such as presenting questions with solutions, etc.

- PyMdown extensions expands default MkDocs syntax, including support for MathJax.

- Integration between MkDocs and Jupyter Notebooks is possible (though needs to be tested in detail.)


## Displaying code

Here are some simple code blocks. They have a built in copy function, which is nice.


### Code no line numbers

``` python
""" Bubble sort """
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

### Code with line numbers

``` python linenums="1"
""" Bubble sort """
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

### Code with line numbers and highlighted lines

``` python linenums="1" hl_lines="3 4"
""" Bubble sort """
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```


### Tabbed code blocks

=== "Step 1"
	``` python
	""" Bubble sort """
	def bubble_sort(items):
	```

=== "Step 2"
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



## Example of MathJax 


$$
\frac{n!}{k!(n-k)!} = \binom{n}{k}
$$

Lorem ipsum dolor sit amet: $p(x|y) = \frac{p(y|x)p(x)}{p(y)}$