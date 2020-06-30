# LaTeX Documentation

This is the documentation for our LaTeX documents.  

[Full LaTeX documentation is available on Wikibooks](https://en.wikibooks.org/wiki/LaTeX)  

This document will cover our custom LaTeX macros and style.  

## Images

There is a custom macro just for our documentation which allows us to easily
add images to the files. Here is an example:

```latex
\mkimg{0.5}{test.png}{A test image}{test}
```

The order of arguments is as follows: width, filename, caption, figure
reference. Note that the last argument will not show on the document, but the
figure can then be referenced. For the example above, you can reference it
like:
```latex
See figure \ref{fig:test} on the page \pageref{fig:test} for an example.
```
However, you do not have to reference the page.


