---
title: Thank god for WSL (Windows Subsystem for Linux)
layout: page
parent: Infrastructure
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

When installing and enabling the Windows Subsystem for Linux (WSL), it's essential to perform these actions as an administrator. However, as reported in [this GitHub issue](https://github.com/microsoft/WSL/issues/9575), even running PowerShell as an administrator may not be sufficient if your currently logged-in user doesn't have administrative rights. In these cases, you may encounter a "Catastrophic failure" error message.

## Use Case

Users logged in to Windows with a non-administrative account, using a separate administrative account to perform tasks that require elevated privileges, may find that the installation of WSL does not proceed as expected. When trying to run the `wsl --install` command from a PowerShell instance opened with administrative privileges, the system may respond with a "Catastrophic failure" error message.

Even after installing a Linux distribution from the Microsoft Store, the installed distribution may not be recognized by the `wsl -l -v` command. The issue seems to persist across various attempts to uninstall and reinstall different components.

## Solution

The issue appears to be tied to permissions. When PowerShell is run as a different user, even with administrative privileges, the system fails to install WSL properly. The solution to this problem is to grant administrative rights to the currently logged-in user and execute the installation commands using that account.

Here are the steps to solve the problem:

1. Log in to your Windows machine with an account that has administrative privileges.
2. Open the User Accounts control panel (you can search for it in the Start Menu).
3. Select the user account that you want to grant administrative privileges to.
4. Click on "Change account type".
5. In the new window, select "Administrator" and then click on "Change Account Type".
6. Log out from the administrative account and log back in to the user account that you just granted administrative privileges to.
7. Open a new PowerShell window and run the `wsl --install` command again.

After following these steps, you should be able to successfully install and enable WSL, as well as install distributions without encountering the "Catastrophic failure" error message.

**Important Note:** Granting administrative privileges to a user account should be done cautiously. Having administrative privileges allows the user to make significant changes to the system, which can lead to potential security risks or system instability if misused. Always ensure you follow your organization's IT policies and best practices.

### Enable WSL

Open PowerShell as Administrator and run:

```powershell
wsl --install
wsl --set-default-version 2
```

### Install a Linux Distribution

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