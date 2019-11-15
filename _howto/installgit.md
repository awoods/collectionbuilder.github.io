---
layout: howto
title: How To Install Git
---

# Installing and Setting Up Git

Git is a distributed version-control system that helps track changes in source coding while you interact with software development. It is really useful in this sort of work, when you may be interacting with multiple persons developing at once. It helps you track and maintain individual files while you work, and its primary goals are speed and efficiency, which is something we value while working with Collection Builder. Git is both free and open-source. 

## Step 1: Installing Git 

- You're going to want to start off by going to the [Git download page](https://git-scm.com/downloads) and click on whichever operating system you utilize. Below is a photo of what this page will look like, along with the OS options you are prompted with. 

- After you click on your OS, a zip file will drop into the corner of your browser, click on it. 

- A security warning will open up, click on "Run". 

- Git's general information and disclaimer will then appear, just keep hitting next until the program begins downloading. 

- Next, a window called "Completing the Git Setup Wizard" will prompt you to click on "finish," click it. 

- You will know you are done when Git's Release Notes come up on your screen. 

## Step 2: Configuring Git

- Now that Git is installed we need to configure it to your personal information. Open your terminal. On Windows search for Git Bash, and on Linux and Mac search for terminal. 

- Once you have a command line open, type ``` git config --global user.name "User Name"``` The "User Name" in this command refers to your GitHub username. Once you have typed this press enter.

- Next you'll need to make sure you have the correct email address configured as well. Type ``` git config --global user.email "Email Address." ``` The email referring to the email you have set to your GitHub account. 
  