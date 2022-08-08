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

There are two options that will allow you to connect to GitHub from your computer; you can either create a personal access token (PAT) and connect via HTTPS (**H**yper**t**ext **T**ransfer **P**rotocol **S**ecure) or you can generate an SSH (**S**ecure **Sh**ell) key for your device. Both, as you may have guessed by the name, are secure ways to transfer files to your GitHub account by letting GitHub know that your personal device can be trusted through a unique and elaborate "key", much like a password.

The significant positive of using a PAT is how simple it is to set up! The negative is that you must keep it stored like a password, because you will need to enter it on any other devices that you intend to connect Git and GitHub on.

If you run into trouble setting up your PAT, then you can also try generating an SSH key for GitHub. This is slightly more complicated to get up-and-running, but you don't have to write anything down since you generate a unique SSH key for every device you would like to connect!

{{< alert icon="👉" context="info" text="<b>Windows Users:</b> To configure Git and perform the initial set up of GitHub on your device, you must use Git Bash which is located under the <q>Git</q> folder that can be accessed from the Start menu. After this step is done you may continue to use the Anaconda Powershell Prompt!" />}}  

## Configuring Git

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

## Option #1: Using a PAT

- On the GitHub website, go to your profile settings which can be accessed by selecting your profile picture in the upper right corner of the page.
- In the left hand menu, scroll down to the bottom and open "Developer settings"
- Select "Personal access tokens", then hit the button which says "Generate new token"

Once on the **"New personal access token"** page you will:
- Set the expiry date for your PAT- this is the interval at which you will have to generate a new PAT. Choose however long you feel comfortable keeping this "password" active for!
- Grant access permissions for this PAT- since you are the admin user of your device that is connecting to your GitHub account, we suggest ticking every checkbox to make sure you do not miss any permissions you may need.

Once your PAT is generated, save it with the rest of your passwords and treat it like one! If you accidentally push it to GitHub in a note file, the PAT will automatically be disabled and you will have to create a new one.

**In the next step of this workshop,** when you enter the `git push` command:
- **On MacOS**: You will be prompted in the command line to enter your GitHub username and password. Enter your username as expected, but **enter your PAT as the password** to connect your account.
- **On Windows**: A login box will open giving you ways to connect to GitHub; select the option which asks to use a PAT and proceed as instructed. 

Should you ever need to remove your PAT to set a new one, you can use the follow comannd to find the PAT:
```
security find-internet-password -l github.com
```
And then this command to delete it:
```
security delete-internet-password -l github.com
```

## Option #2: Using an SSH key

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