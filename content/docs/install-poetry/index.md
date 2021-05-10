---
title: 'Install Poetry'
date: 2019-02-11T19:27:37+10:00
draft: false
weight: 3
summary: Install Poetry, create a new project, add a module with dependency to the package using Poetry.
---


### Install Poetry on Ubuntu 20.04

1. Open a terminal, activate the virtual environment, and type the following command:

    ```curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/install-poetry.py | python3 -```

    An output similar to the following appears:
     ![image](/images/poetry_terminal.png)

1. Verify  the version of Poetry that is installed using the command:
    ``` poetry --version```


#### Create a New Project and Add Dependency

In the following steps you create a new project named **demo**, add a module **place.py** with a dependency **arrow** to the package **greet**.

1. Create a new project *demo* with the package *greet* in the *src* directory.:

    ```poetry new --name greet --src demo```

    A new directory named *demo* is created with a standard python folder structure.

2. Change to the *demo* directory and type `tree`

      An output similar to the following appears:

      ![image](/images/poetry_structure.png)

3. Create a module **place.py** with an editor of your choice using the command ```sudo nano src/greet/place.py```

4. Add the following lines to the **place.py** file.
    ```
    """Send greetings."""

    import arrow

    def greet(tz):
        """Greet a place."""
        now = arrow.now(tz)
        friendly_time = now.format("h:mm a")
        place = tz.split("/")[-1].replace("_"," ")
        return f"Hello, {place}! The time is {friendly_time}."

    ```
    The code in **place.py** contains a date library dependency [arrow](https://pypi.org/project/arrow/) that needs to be installed.

5. Add the dependency *arrow* to the pakage, using `poetry add arrow`.

6. Install the package and dependencies, using `poetry install`.

7. Execute the command in the virtual environment, to verify if the installed dependency works in the package.

```
[demo]$ poetry run python
>>> from greet.place import greet
>>> greet("Asia/Kolkata")
'Hello, Kolkata! THe time is 4.05 am.'
>>>
```

You can use Poetry to builb, publish, and even track your project. For additional information about the various commands that you can use with Poetry, see the [Official Documentation](https://python-poetry.org/docs).

