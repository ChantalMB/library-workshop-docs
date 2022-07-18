---
title: "Pre-Workshop Tasks"
description: "Please complete these activities prior to attending the workshop."
lead: "Please complete these activities prior to attending the workshop."
date: 2020-11-12T13:26:54+01:00
lastmod: 2020-11-12T13:26:54+01:00
draft: false
images: []
menu:
  docs:
    parent: "workshop-I"
weight: 510
toc: true
---

### *Read*
[The Schism at the Heart of the Open-Source Movement](https://www.theatlantic.com/technology/archive/2020/01/ice-contract-github-sparks-developer-protests/604339/) by Sidney Fussell

### *Do*

> **For those using Apple devices**: You can make the installation of the following list very quick and easy by first installing [Homebrew](https://brew.sh/). Search "terminal" using Spotlight or in Finder, open the application, then paste the command featured centerally on the linked webpage (hit the little clipboard beside it) and hit enter! I will provide the installation commands for each item listed below that you can enter into the terminal after installing Homebrew.

> {{< alert icon=":mega:" context="warning" text="<b>Beware:</b> Depending on your internet connectivity, Homebrew can take a <i>long</i> time to install. Best to just run the command and carry about your day, checking on it every so often to make sure there's no error message. If you receieve an error message that you cannot decipher, take a screenshot of your command line and send it to Chantal or Martha so we can help you troubleshoot!" />}}

- **Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html)**
  - You likely want the 64-bit version
  - This is a "command line environment", which essentially means that having this installed allows us to create a container for all of our tech work so that even if something was to go wrong, it would only be in the container and not effect the rest of your computer!
  - **Windows Users:** From this download, we will be using the Anaconda3 ***Powershell*** Prompt!
  - Homebrew installation command:
  	```
    brew install --cask miniconda
    ```
- **Download [Visual Studio Code](https://code.visualstudio.com/)**
  - More commonly referred to as "VS Code", this is a "text editor" which allows you to write notes in Markdown (a markup language that many web-based platforms use, such as this website).
  - Homebrew installation command:
    ```
    brew install --cask visual-studio-code
    ```
	 
- **Install [Git](https://git-scm.com/downloads)**
  - Git is a version control software, which is a fancy way of saying it lets you save your projects at any point in the process of creation, and if something goes wrong you can revert the project back to any one of these saved points. We use it via the command line, because instead of tracking and saving just a single file, it does so for a whole folder on your desktop!
  - Homebrew installation command:
    ```
    brew install git
    ```
- **Create a [GitHub account](https://github.com/)**
  - Github is a repository hosting tool for the projects you save and track with Git. It allows you to publicly share your work.