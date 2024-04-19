# Python boilerplate repostiroy

This repository contains boilerplate for a research repository with continuous integration using GitHub actions. To use this code for your own project, make sure to find-and-replace all places where `my_package` is used with your own package name.

## Project structure

All Python code is under the `my_package` package. Run

    pip install -e .

to install dependencies. Dependencies can be added in `pyproject.toml`.

## Linting/formatting/type checking/testing

When commits are pushed to GitHub, they are checked with the [Flake8 linter](https://flake8.pycqa.org/en/latest/), [Black code formatter](https://black.readthedocs.io/en/stable/), [isort import sorter](https://pycqa.github.io/isort/index.html), and [Mypy type checker](http://mypy-lang.org/). Tests are also run with [pytest](https://docs.pytest.org/en/7.2.x/). To install these tools locally, run

    pip install --upgrade -e .[dev]

Then, they can be run by `./lint.sh`. To run tests, run `pytest`.

### Python version

This repository is by default configured to target Python 3.9 and test in Python versions 3.8 to 3.10. To change the target Python version, modify the line `python_version = 3.9` in `mypy.ini` and the line `target-version = ['py39']` in `pyproject.toml` (under `[tool.black]`). To change the versions that are tested in the GitHub workflow, modify the line `python_version: ['3.8', '3.9', '3.10']` in `.github/workflows/ci.yml`.
