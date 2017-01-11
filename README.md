# pandoc-shortcaption filter

`pandoc-fignos` is a [pandoc](http://pandoc.org/) filter for adding short captions to LaTeX output.

## Installation

~~~
pip install pandoc-shortcaption
~~~

or

~~~
python setup.py install
~~~

## Basic usage

~~~
![This is a long image caption](img.png "Image Short Caption")
~~~

Compile with
~~~
pandoc -f markdown -t latex --filter pandoc-shortcaption  test.md
~~~

If you would like to use with [pandoc-crossref](https://github.com/lierdakil/pandoc-crossref), then add that filter afterwards.

~~~
![long caption again](img.png "short caption"){#fig:myfig2}

Here is a reference to @fig:myfig2.
~~~

and compile with

~~~
pandoc -f markdown -t latex --filter pandoc-shortcaption --filter pandoc-crossref test.md
~~~


## Acknowledgments and references

Inspired by [Template for writing a PhD thesis in Markdown](https://github.com/tompollard/phd_thesis_markdown).

* [Python Apps the Right Way: entry points and scripts](https://chriswarrick.com/blog/2014/09/15/python-apps-the-right-way-entry_points-and-scripts/)
*  [pandocfilters](https://github.com/jgm/pandocfilters)

