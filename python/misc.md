# imports

never import `*`.

Eg: `from foo.bar import *` is nasty

# docstrings

paste this into a Python terminal

```
def hi_there(stuff):
    """this is a docstring
    it can take up
    multiple lines
    """
    pass


help(hi_there)
```

Docstrings are great because the Python help system is aware of them. 