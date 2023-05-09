---
title: Thank god for WSL (Windows Subsystem for Linux)
layout: page
parent: infrastructure
---

# Thank god for WSL (Windows Subsystem for Linux)

## Cheat Sheet

1. A Brief History: Windows for Development
2. What is WSL?
3. How to Install WSL
4. WSL in Windows Terminal and VSCode
5. Switching between PowerShell and WSL

Now, let's dive in!

## 1. A Brief History: Windows for Development

Once upon a time, Windows was not the first choice for developers. Unix-based systems, like Linux and macOS, offered a more friendly environment for programming, particularly for web development and scripting. The command line interface in Unix-based systems was more powerful, flexible, and integrated with development tools compared to the Windows Command Prompt or PowerShell.

However, the landscape has changed dramatically in recent years, largely thanks to the introduction of the Windows Subsystem for Linux (WSL) and enhancements to the Windows Terminal and VSCode. These developments have made Windows an increasingly attractive platform for developers.

## 2. What is WSL?

The Windows Subsystem for Linux (WSL) is a compatibility layer for running Linux binary executables natively on Windows 10 and Windows Server 2019. In simpler terms, WSL allows developers to run a GNU/Linux environment directly on Windows, without the overhead of a virtual machine.

There are two versions of WSL. WSL 1 is a translation layer on the Windows kernel, whereas WSL 2 runs a full Linux kernel in a lightweight virtual machine, offering 100% system call compatibility, and near-native performance.

> Note: WSL does not include a Linux kernel on install; you have to download a distribution, like Ubuntu, from the Microsoft Store.

## 3. How to Install WSL

### Step 1: Enable WSL

Open PowerShell as Administrator and run:

```powershell
wsl --set-default-version 2
```

### Step 2: Install a Linux Distribution

Visit the Microsoft Store and search for "Linux". Select your preferred distribution (for example, "Ubuntu") and click "Install".

Once the installation is complete, launch the distribution from the Start menu. The first time you launch it, it will complete the installation and prompt you to create a new user account.

> Tip: If you encounter any issues during installation, refer to the official [WSL installation guide](https://docs.microsoft.com/en-us/windows/wsl/install-win10).

## 4. WSL in Windows Terminal and VSCode

The introduction of Windows Terminal, a modern terminal application with support for tabs, rich text, and customization, has further bridged the gap between Windows and Unix-like systems. Windows Terminal can run any command-line application, including WSL distributions, Command Prompt, and PowerShell.

Visual Studio Code (VSCode) has also integrated WSL into its operations. With the "Remote - WSL" extension, you can open any folder in the WSL and take advantage of VSCode's full feature set for your Linux-based projects.

## 5. Switching between PowerShell and WSL

Switching between PowerShell and WSL in Windows Terminal is as simple as opening a new tab. Each tab in Windows Terminal can run a different shell, so you can have PowerShell in one tab and Ubuntu in another. This flexibility allows you to utilize the strengths of each environment and seamlessly switch back and forth depending on your needs.

> Tip: You can even use Linux commands in PowerShell by prefixing them with `wsl`, like `wsl ls`.

| Command | Description |
|---------|-------------|
| `wsl --set-default-version 2` | Enable WSL 2 |
| `wsl ls` | Use a Linux command in PowerShell |

Windows is no longer a second-class citizen in the world of development