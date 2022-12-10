
---
title: How to set up Python on Windows
layout: page
parent: Coding
nav_order: 1
---

# How to set up Python on Windows
{: .This page }
Developing on Windows can be tricky. This doc outlines how to set up a functional development environmet on Windows.

## Cheat Sheet
Use Chocolatey as a package manager for Windows
1. Open admin command prompt
    '''cmd
    Set-ExecutionPolicy Bypass -Scope Process
    '''
2. Install Chocolatey
    '''cmd
    Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
    '''
3. Install Python
    '''cmd
    choco install python3
    '''

## Windows App Store
Windows has added Python to their app store. While this may seem attractive because it's easy and convenient to install and manage, it makes developing a pain because your path and folders are note set up for things like `pip` and `virtualenv`.

## Recommended method of installation
The recommended method of installation is to use the [Chocolatey](https://chocolatey.org/) package manager. Chocolatey is a package manager for Windows. It's similar to `apt-get` on Linux and `brew` on Mac. It's a great way to install and manage software on Windows.

### Install Chocolatey
First we need to change your execution policy since Windows will block Chocolatey from running by default. Open a command prompt as an administrator and run the following command:

    Set-ExecutionPolicy Bypass -Scope Process

Then install Chocolatey by running the following command:

    Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1')) 


### Install Python
To install Python, open a command prompt as an administrator and run the following command:

    choco install python3

## Next steps
### Install:
### Visual Studio Code
### GitHub Desktop
### virtualenv
### pipenv
### Windows Subsystem for Linux (WSL)