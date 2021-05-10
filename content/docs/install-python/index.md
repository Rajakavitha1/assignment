---
title: 'Install Python3'
date: 2019-02-11T19:27:37+10:00
weight: 2
summary: One of the prerequisite to use Poetry is to install Python3.
---

To use Poetry you need to have Python installed. If you don't already have Python3 installed follow the official [installation guide](https://wiki.python.org/moin/BeginnersGuide/).

### Check Python Version

 Python 3.5 will no longer be supported in the next feature release 1.2 of Poetry. Hence, it is recommended to install the version of Python later than 3.5.
```
python --version
```
### Create a Virtual Environment

To create a virtual environment, decide upon a directory where you want to place it, and run the `venv` module as a script with the directory path:

```python3 -m venv poetry-env```

This creates the `poetry-env` directory and also creates directories that contain a copy of the Python interpreter, the standard library, and various supporting files.

### Activate the Virtual Environment

When you activate the virtual environment the system changes the shell prompt to reflect the virtual environment that you’re using. It also modifys the environment such that when you run python the system provides you with a particular version and installation of Python.

```source poetry-env/bin/activate```