---
title: "Working in the Command Line"
description: "A reference for common commands used when working with the command line interface (CLI)."
lead: "A reference for common commands used when working with the command line interface (CLI)."
date: 2020-11-12T13:26:54+01:00
lastmod: 2020-11-12T13:26:54+01:00
draft: false
images: []
menu:
  docs:
    parent: "workshop-I"
weight: 520
toc: true
---

## Command Line Basics
| Mac & Linux       | Windows Powershell         | Use         |
| ----------------- | ----------------- | ----------- |
| `cd [path_to_file]` | `cd [path_to_file]` | **c**hange **d**irectory-- go to a different folder on your computer (*hint*: to go back a step type `..`) |
|  `ls`             | `ls`                | **l**i**s**t all the files in the folder you're currently in  |
| `pwd`               | `pwd`               | **p**rint **w**orking **d**irectory-- if you forget what folder you're in, type this and the command line will tell you where you are |
| `mkdir [folder]`    | `mkdir [folder]`    | Creates a new directory (aka folder) in the directory you're in |
| `man [command]`     | `help [command]`    | Tells you what a command does by outputting the documentation for it |

## Keyboard Shortcuts for the Command Line
| Command       							| Use         |
| --------------------------- | ----------- |
| `ctrl` + `c`										| **C**ancels the command that is currently running, meaning that the command will stop whatever it's doing immediately. |
| `up` and `down` arrow keys	| Allows you to see (and re-run) commands you have previously typed |
| `tab`   											| Auto-completes file or path names based on the directory you're in.  |

## Common Conda Commands
| Command    							   		 										| Use         |
| ------------------------------------------------- | ----------- |
| `conda create --name [your_environment_name]`   		| Creates a new conda environment for you to work in. |
|	`conda install [package name]`  							  		| Installs a package into your conda environment. |
|	`conda list` 																	 		  |	Lists all of the packages installed in your current, active environment |
|	`conda env list` 															  		|	Lists all of the conda environments you've created |
|	`conda env remove --name [your_environment_name]`   | Deletes an environment and everything in it. |

**For more commands and resources,** see the [full `conda` cheat sheet](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf).

## Bonus (MacOS): Styling Your Command Line
Black-on-white can be difficult to read and harsh on the eyes, so you may want to consider giving it a more friendly colour scheme! To do so, download your favourite theme from [this repository and follow the installation instructions also provided in the `README`.](https://github.com/lysyi3m/macos-terminal-themes)

## Bonus (Windows): Windows Terminal for "All-in-One" CLI
Unlike the command line "shells" such as `zsh` or `bash` found on UNIX-based operating systems such as MacOS or Linux, Windows created its own version, Powershell. Powershell makes things a bit complicated for programming because it requires all command line tools to install their own separate CLIs (ex Anaconda Powershell Prompt, rather than being accessible from just the single Windows Powershell Prompt! 

Microsoft has recently released [Windows Terminal](https://apps.microsoft.com/store/detail/windows-terminal/9N0DX20HK701?hl=en-ca&gl=CA) as somewhat of a solution to keeping all your tools in one place-- you can add all your various CLIs into this terminal and open them in separate tabs rather than separate windows!

- [Here is a guide to adding Git Bash](https://www.timschaeps.be/post/adding-git-bash-to-windows-terminal/)
- [Here is a guide to adding Anaconda Powershell Prompt](https://medium.com/@shouke.wei/windows-python-developers-had-better-setup-earlier-iv-add-anaconda-powershell-on-windows-8942dd9cc1a)
