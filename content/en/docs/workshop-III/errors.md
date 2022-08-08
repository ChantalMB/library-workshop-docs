---
title: "Common Errors"
description: "Explaining some errors you may encounter as you advance in your programming journey!"
lead: "Operators for comparing data types."
date: 2020-11-12T13:26:54+01:00
lastmod: 2020-11-12T13:26:54+01:00
draft: false
images: []
menu:
  docs:
    parent: "workshop-III"
weight: 720
toc: true
---

## Common Python Errors
> **Reminder**: Read the whole error message! Python often points to the line where the error is at the beginning of the message, and at the end when it states the type of error, also often offers a suggestion to fix the error.

| Error               | Meaning | Solution? |
| ------------------- | ------- | --------- |
| ModuleNotFoundError | Python couldn't find the thing you tried to import | At the top of your notebook create a new cell and enter `!pip install [the module that could not be found]`, then run to install or update the missing module |
| SyntaxError         | You're missing something vital to how the Python langauge must be written in order to be understood by the computer | Check for small things like a missing ":" in a loop or `if` statement, or missing parentheses |
| IndexError          | You attempted to access a position in a list that doesn't exist | Remember that in Python, counting starts at 0, so if you have 3 items in your list and you want to access the final item, it would look like `list[2]` **not** `list[3]` |
| TypeError           | You tried to use a certain data type in a situation where it cannot be used | Did you perhaps try to add a string and an integer together? Or concatenate a string where one of the variables in the concatenation is something other than a string? |
| NameError           | An object you tried to use could not be found | You likely tried to use a variable and either misspelled or forgot to declare it! |

**If none of these solutions help**, try using this formula to perform a Google search:
| python "[error message]" solution |
| --- |
