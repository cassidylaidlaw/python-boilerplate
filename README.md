# Python boilerplate repostiroy

This repository contains boilerplate for a research repository with continuous integration using GitHub actions. To use this code for your own project, make sure to find-and-replace all places where `my_package` is used with your own package name.

## Project structure

All Python code is under the `my_package` package. Run

    pip install -r requirements.txt

to install dependencies.

## Linting/formatting/type checking/testing

When commits are pushed to GitHub, they are checked with the [Flake8 linter](https://flake8.pycqa.org/en/latest/), [Black code formatter](https://black.readthedocs.io/en/stable/), [isort import sorter](https://pycqa.github.io/isort/index.html), and [Mypy type checker](http://mypy-lang.org/). Tests are also run with [pytest](https://docs.pytest.org/en/7.2.x/). To install these tools locally, run

    pip install --upgrade -r requirements_dev.txt

Then, they can be run by `./lint.sh`. To run tests, run `pytest`.
