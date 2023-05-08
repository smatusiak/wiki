---
title: Microsoft Win32 Content Prep Tool
layout: page
parent: infrastructure
---

# Microsoft Win32 Content Prep Tool

The Microsoft Win32 Content Prep Tool is a tool that can be used to prepare Win32 applications for deployment via Intune. This tool takes the application files and creates a .intunewin file that can be uploaded to Intune and then deployed to Windows 10 devices. The tool is available on GitHub and can be downloaded and used by anyone looking to deploy Win32 applications via Intune.

## Usage Examples

Here's an example of how you might use the tool to deploy an application via Intune:
1. Download the Microsoft Win32 Content Prep Tool from GitHub and install it on your computer.
2. Run the tool and select the application files you want to deploy.
3. The tool will create a .intunewin file that can be uploaded to Intune.
4. In the Intune portal, create a new Win32 app and upload the .intunewin file.
5. Assign the app to the desired group of devices and deploy it.

## Code Snippets

Here are some sample commands for using the Microsoft Win32 Content Prep Tool, taken from the tool's README on GitHub:

```
IntuneWinAppUtil -v
```
This will show the tool version (Only available starting version 1.8.2).

```
IntuneWinAppUtil -h
```
This will show usage information for the tool.

```
IntuneWinAppUtil -c <setup_folder> -s <source_setup_file> -o <output_folder> <-q>
```
This will generate the .intunewin file from the specified source folder and setup file. For MSI setup file, this tool will retrieve required information for Intune. If -a is specified, all catalog files in that folder will be bundled into the .intunewin file. If -q is specified, it will be in quiet mode. If the output file already exists, it will be overwritten. Also if the output folder does not exist, it will be created automatically.

```
IntuneWinAppUtil
```
If no parameter is specified, this tool will guide you to input the required parameters step by step.

Is there anything else you would like me to include in the blog post?

Source: Conversation with Bing, 2023-05-08(1) microsoft/Microsoft-Win32-Content-Prep-Tool - Github. https://github.com/microsoft/Microsoft-Win32-Content-Prep-Tool Accessed 2023-05-08.
(2) Releases: microsoft/Microsoft-Win32-Content-Prep-Tool - Github. https://github.com/Microsoft/Microsoft-Win32-Content-Prep-Tool/releases Accessed 2023-05-08.
(3) Deploying Apps in Intune – Part 2 – The Win32 Content Prep Tool. https://webber.zone/2022/10/02/deploying-apps-in-intune-part-2-the-win32-content-prep-tool/ Accessed 2023-05-08.