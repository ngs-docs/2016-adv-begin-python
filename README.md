# Advanced Beginner Python

Materials for [Advanced Beginner
Python](https://dib-training.readthedocs.org/en/pub/2016-04-04-adv-beg-python.html),
offered Apr 4th, 2016, at UC Davis.

These materials are, roughly, meant to be a follow-on from Software
Carpentry's [Programming with
Python](https://swcarpentry.github.io/python-novice-inflammation/).
They are under CC0 Waiver - no copyright is claimed.  Use and reuse are
freely allowed.

A long, long time ago (in 2007), I offered a 3 day workshop at
Lawrence Livermore called "Intermediate and Advanced Software
Carpentry in Python."  [Those materials are also freely
available](http://ivory.idyll.org/articles/advanced-swc/) but a bit out
of date.

These will be "stub notes" - associated discussion and code will be

* [in the Etherpad](https://etherpad.wikimedia.org/p/2016-adv-begin-python)
* [in the source code repository](https://github.com/ngs-docs/2016-adv-begin-python-source)

## Welcome to the workshop!

* WHOAMI?
* Materials stay up indefinitely.
* This workshop being live-streamed and recorded.
* Goals: show you the tools, work through them, provide foil for questions.
* We have a [Code of conduct](http://software-carpentry.org/conduct/)
* We'll have a coffee break!
* If you don't have a working Python install you can use [this](http://mybinder.org/repo/ctb/2016-mybinder-inflammation)

## Data and problem

* we'll be counting Ns - it's going to be very exciting!
* we'll be using `this FASTQ file of data <https://github.com/ngs-docs/2016-adv-begin-python-source/raw/master/ecoli_ref-100k.fq.gz>`__
* you can download it directly with `curl -L -O https://github.com/ngs-docs/2016-adv-begin-python-source/raw/master/ecoli_ref-100k.fq.gz`

## Code reuse and modules

* modules provide namespaces for functions, variables, etc.
* they are a simple element of code reuse.
* I organize my code into scripts and modules.
* scripts coordinate execution of code.
* modules provide reusable functions that (usually) multiple scripts use.
* `if __name__ == '__main__'` is only run on execution, not on import.
* my convention is to use something like 'main()' as the main function,
  executed in the `__main__` block.
* you can build packages by putting multiple modules in a directory,
  then placing an `__init__.py` file in there.
* argparse is a great way to parse command-line arguments.
* `#! /usr/bin/env python3.x` is a good way to start scripts.

## Testing and automated tests

* once you have code that you use in multiple places, you should put more
  emphasis on making sure it works.
* 'assert' statements make assertions about the state of variables at a
  given point in time.
* Assert statements are invaluable ways to guard your back against weird/
  unexpected use of code in future situations.  They do little harm.
* functions named 'test_' is generally how Python folk label test code.
* you can use 'nose' or 'py.test' to run all functions named 'test_*'.
* 'test_' functions are unit tests that set up a specific condition and
  run your code on it.
* start simple.
* no, really, start simpler than you think is worthwhile.
* if your most basic tests fail, then you really have a problem, don't you?
* code coverage is a good way to target additional tests; see [coverage docs](https://coverage.readthedocs.org/) for the Python package to use

## 'virtualenv'

* "virtualenv" is a great tool for creating collections of installed packages
  that will never change.
* create a virtualenv with `python -m virtualenv NAME`
* activate a virtualenv with `. NAME/bin/activate` (in bash).
* deactivate with `deactivate`
* pip to install code.
* if you use `#! /usr/bin/env python` this will work within virtualenvs.

## Fun Python tricks

* run modules in specific versions of Python with `python -m`.
* generators: put 'yield' in a Python function to turn it into a generator.
* check out 'enumerate'!

## Other principles

* make a cut-down data set so that you can iterate quickly when doing data analysis
* display progress indicators for long analyses.
