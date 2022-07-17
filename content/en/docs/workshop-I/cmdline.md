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