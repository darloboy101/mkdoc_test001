# Welcome

We're considering using [MkDocs](https://www.mkdocs.org) with the [Material theme](https://squidfunk.github.io/mkdocs-material/) as the basis for displaying some of the content within the distance learning AI module. 

Some of the advantages we've identified are:

- MkDocs is Python based and can be installed using Pip. Docker images for Mkdocs with material are available. As such, should be convenient for DES and Computer Science to use.

- Material theme is adaptable and provides a high standard of accessibility and mobile usability out of the box.

- Content will be authored in Markdown. Git integration means that content management / version control between Computer Science and the DES should be straightforward to manage.

- Content will be processed to a static site that can be hosted from the Minerva content collection. This will significantly simplify requirements for the hosting / maintenance of content. 

- International students with bandwith challenges should be able to download content to view locally. It should be possible to process MkDocs content to additional formats, such as PDF and ePub. 

- Robust support for displaying Python code samples using Pygments and CodeHilite.


- Admonition extension allows block-styled content that supports pedagogical uses such as presenting questions with solutions, etc.

- PyMdown extensions expands default MkDocs syntax, including support for MathJax.

- Integration between MkDocs and Jupyter Notebooks is possible (though needs to be tested in detail.)

- Mermaid is a available as a plugin integration for MkDocs if sequence diagrams are required.