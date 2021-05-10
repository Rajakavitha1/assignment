---
title: 'Configuration'
date: 2019-02-11T19:30:08+10:00
draft: false
weight: 4
summary: Details about the sections and the various options that can be configured in the `pyproject.toml` file.
---

## pyproject.toml

The secret to manage dependencies and packages in a Poetry project is contained in a file called `pyproject.toml`. This is where you define the metadata, dependencies, scripts, and more.  The `pyproject.toml` replaces `setup.py`, `requirements.txt`, `setup.cfg`, `MANIFEST.in`, and `Pipfile`. In  other words `pyproject.toml` is the Python equivalent of `package.json` in Node.

At minimum the `pyproject.toml` contains the following content:

````
[tool.poetry]
name = "greet"
version = "0.1.0"
description = ""
authors = ["Rajakavitha Kodhandapani <hello@rajie.space>"]

[tool.poetry.dependencies]
python = "^3.7"
arrow = "^1.1.0"

[tool.poetry.dev-dependencies]
pytest = "^5.2"

[build-system]
requires = ["poetry-core=1.0.0"]
build-backend = "poetry.core.masonry.api"
````

The four primary sections in a `pyproject.toml` file are:

- **[tool.poetry]** : Contains metadata of the package, such as the package name, description, author details, and others.
- **[tool.poetry.dependencies]** : Contains the dependencies that the application absolutely must download to run. You may specify specific version numbers for required packages (such as python = "^3.7"), or to grab the latest version, set the value to "*" .
- **[tool.poetry.dev.dependencies]**: Contains the development dependency packages that other developers should download to contribute to the project.
- **[buils-system]**: Contains the details of the build-system that is required to build, manage, or tack the project.

For additional information about the various sections and the options that you can define in `pyproject.toml`, see the [Official Documentation](https://python-poetry.org/docs/pyproject/).