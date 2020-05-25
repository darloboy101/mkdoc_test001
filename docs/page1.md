# Step 1

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Displaying code

Here are some simple code blocks. They have a built in copy function, which is nice.


<iframe src="https://trinket.io/embed/python3/04f5c0691b" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>



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



## Test of video

<div class="video-wrapper">
  <iframe width="1280" height="420" src="https://www.youtube.com/embed/vZNyjuNLhIk" frameborder="0" allowfullscreen></iframe>
</div>

## Example of MathJax 


$$
\frac{n!}{k!(n-k)!} = \binom{n}{k}
$$

Lorem ipsum dolor sit amet: $p(x|y) = \frac{p(y|x)p(x)}{p(y)}$


## Examples of blocks

!!! Question
    This is where a question could be asked.

??? note "Answer"
    This is the code

    ``` python
		import tensorflow as tf
	```

	$$
	\frac{n!}{k!(n-k)!} = \binom{n}{k}
	$$
