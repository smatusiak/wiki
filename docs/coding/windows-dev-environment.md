---
title: Setting Up a Python Development Environment in Windows
layout: page
parent: Coding
---

# Setting Up a Python Development Environment in Windows

## Quick Reference

1. Install Python
2. Install pip
3. Install virtualenv
4. Create a virtual environment
5. Activate the virtual environment
6. Deactivate the virtual environment

Now, let's walk through the detailed guide to setting up a Python development environment in Windows.

## 1. Install Python

Python can be installed either via the Windows Store or using winget.

### Windows Store

Python is available for direct download and installation from the Windows Store. This option simplifies the installation process and automatically manages updates.

1. Open the Windows Store.
2. Search for "Python".
3. Click on "Get" to install the latest version.

### Winget

Winget, a package manager for Windows, simplifies software installation. If winget is installed on your machine, you can install the latest Python version with the command:

```bash
winget install Python
```

To install a specific Python version, use the `-v` option followed by the version number:

```bash
winget install Python -v [version-number]
```

> Note: Python installed via the Windows Store or winget is automatically added to PATH.

## 2. Install pip

Pip, the Python package manager, may not be installed with Python in some cases. To install pip, download the [get-pip.py](https://bootstrap.pypa.io/get-pip.py) file and run it using Python:

```bash
python get-pip.py
```

To verify the installation, run:

```bash
pip --version
```

## 3. Install virtualenv

Virtualenv, a tool for creating isolated Python environments, can be installed using pip:

```bash
pip install virtualenv
```

## 4. Create a Virtual Environment

To create a new virtual environment in your project directory, run:

```bash
virtualenv venv
```

This command creates a new folder named 'venv' that houses the virtual environment.

## 5. Activate the Virtual Environment

To activate the virtual environment, run:

```bash
venv\Scripts\activate
```

The command prompt should now start with `(venv)`, indicating that the virtual environment is active.

## 6. Deactivate the Virtual Environment

You can deactivate the virtual environment when you're finished working on your project with:

```bash
deactivate
```

> Tip: Always remember to activate your virtual environment before starting your project and deactivate it when you're done!

| Command | Description |
|---------|-------------|
| `python get-pip.py` | Install pip |
| `pip --version` | Check pip version |
| `pip install virtualenv` | Install virtualenv |
| `virtualenv venv` | Create a new virtual environment named 'venv' |
| `venv\Scripts\activate` | Activate the virtual environment |
| `deactivate` | Deactivate the virtual environment |

Congratulations! You have successfully set up a Python development environment in Windows, equipped with virtualenv and pip. Happy coding!