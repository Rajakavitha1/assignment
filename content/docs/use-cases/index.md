---
title: 'Use Cases'
date: 2019-02-11T19:27:37+10:00
weight: 5
summary: Details some of the scenarios where you can use Poetry.
---



## Consistent Python environment

Use Poetry to ensure that the Python environments are consistent across different local development environments, cloud-based jobs, and any production environments that you may have. While this is achievable in many different ways, Poetry makes it simple.

## Keep a Check on Dependencies

If you install the dependencies through Poetry then an upstream change to a dependency cannot cause unexpected issues, because Poetry helps you understand the dependency graph of the project so you can understand why each package is installed.

## Easy for Data Scientists

Data Scientists and beginners to Python programming language find it overwhelming to manage package dependencies and publish the project on PyPI or other form of package registry. There are too many tools involved in the ecosystem: virtualenv, pip, pipenv, flirt, twine, and others. Also they have to often juggle between several tools to get to the end. Poetry makes it easy by managing the dependencies and lets the Data Scientists focus on wrangling data.

# <a name="Dependencies Management Tools"></a>Comparision Table

The following table lists some of the features of the most popular dependency management tools and their availability.

| Feature| npm | pip | pipenv | poetry |
| :-------------- | :-------------- | :----------: | ----------: | :-------------- |
| Access to main repo         | yes          |  yes    | yes | yes          |
| Top level dependencies          | yes          | no    | Pipfile | pyproject.toml          |
| Development dependencies | yes          |   no    | Pipfile | pyproject.toml          |
| Lock versions of dependencies          | yes          |    yes    | Pipfile.lock | poetry.lock          |
| Switch between interpreter versions          | nvm      |    no    |   no | yes          |
| Publishing          | yes         |    no    |      yes | yes          |
| Scripts          | yes          |    no   | Pipfile | no          |
| Editable local packages          | yes          |    yes   |      yes | yes          |
| Integration with Intellij          | yes          |    yes   | partial | no          |

**Note:** This is a comparision table based on the availability of these features in NIX systems.

