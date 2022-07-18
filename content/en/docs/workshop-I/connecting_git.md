---
title: "Connecting Git and GitHub"
description: "Steps for connecting Git (local to your device) to GitHub (on the web)."
lead: "Steps for connecting Git (local to your device) to GitHub (on the web)."
date: 2020-11-12T13:26:54+01:00
lastmod: 2020-11-12T13:26:54+01:00
draft: false
images: []
menu:
  docs:
    parent: "workshop-I"
weight: 540
toc: true
---

So GitHub knows that your personal device can be trusted, you must generate a SSH (**S**ecure **Sh**ell) key for your device which will then be added to your GitHub account so that you may upload and modify your work from your desktop.

{{< alert icon="👉" context="info" text="<b>Windows Users:</b> To configure Git and perform the initial set up of GitHub on your device, you must use Git Bash which is located under the <q>Git</q> folder that can be accessed from the Start menu. After this step is done you may continue to use the Anaconda Powershell Prompt!" />}}  

### Configure
These commands modify the configuration file (aka Settings) for Git, hence calling `git config`. The flag `--global` means that these configurations will only be applied to the user account you're logged into, rather than to every account on your device (assuming there's multiple).
- To add a username associated with your device's Git profile (tip: use your Github username so this is easy to remember):
  ```
  git config --global user.name "Your GitHub name here"
  ```
- To add an email associated with your device's Git profile (use the same email you used for Github):
  ```
  git config --global user.email "your_email@example.com"
  ```
- To make Git output use colour (easier to read):
  ```
  git config --global color.ui true
  ```
### Generate the SSH key
Enter:
  ```
  ssh-keygen -t ed25519 -C "your_email@example.com"
  ```
  - `ssh-keygen`: Command to let your computer know that you want to generate a SSH key
  - `-t`: Flag that stands for 'type'
  - `ed25519`: The 'type' of SSH key aka the algorithim used to generate it
  - `-C`: Attaches your email to this key as a 'comment'

If you are prompted for a file location, just hit enter so your SSH key is saved at the default location on your device.

### Add SSH key to GitHub
- Start the SSH-agent in the background so that your SSH key will be active:
  ```
  eval "$(ssh-agent -s)"
  ```
  This will return something along the lines of `Agent pid [some numbers]`.
- Add your SSH key to the active agent:
  ```
  ssh-add ~/.ssh/id_ed25519
  ```
- Copy the SSH key to your clipboard:
  
  **For Windows:**
  ```
  clip < ~/.ssh/id_ed25519.pub
  ```

  **For Mac:**
  ```
  pbcopy < ~/.ssh/id_ed25519.pub
  ```

Now that your SSH key is activated and copied to your clipboard, in your browser go to GitHub. Go to your account settings,which are accessible from the dropdown menu that appears when you click your icon in the upper right corner of the webpage. In settings, select "SSH and GPG Keys" from the menu to the left, then click the green "New SSH key" button. In the smaller input box enter a nickname for the device which your SSH key is associated with, and in the larger input box paste your SSH key.