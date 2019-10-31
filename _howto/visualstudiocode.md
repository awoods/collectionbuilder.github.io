---
layout: howto
title: How To Install and Set Up Visual Studio Code
---
# How to Install Visual Studio Code

Visual Studio Code is an open source text editor which will help you develop your Collection Builder template. It is a simple platform to edit and push collections projects to GitHub, and is a great program to satisfy the first "Software and Installation Setup" step, which is to obtain a viable text editor. Though several exist, and will serve Collection Builder's function, Visual Studio Code seems to be the most intuitive, versatile, and competent text editor for our purposes. 

## Step 1: Download File

- Go to Visual Studio Code's [website](https://code.visualstudio.com){:target="_blank"}. Here you will find clear instructions about how to download this program. The website should discern if you are visiting their site using windows, IOS, or Linux. 
- It will then display a button that says "Download" for whatever operating system your computer utilizes. Click this button. 

{% include bootstrap/figure.md img="howto/visualstudio/screen-shot-1.png" caption="click download button (provides options for various operating systems)" alt="screen shot of the download button for downloading VS code" class="w-50"%}



## Step 2: Initiate/ Finalize Download

- After you click on the download button you will be taken to a page that says "Get Started." It will also drop a download package to the bottom of your browser (or the top of your browser in the downloads file if using a Mac). 
- Click on the downloaded file and accept the terms of agreement, select the destination location, select menu start folder, click any additional tasks (probably only "add to path"), and then install. 
{% include bootstrap/figure.md img="howto/visualstudio/screen-shot-2.png" caption="click this download file" alt="screen shot of the download file for downloading VS code" class="w-50"%}
- After a minute or so the download should be completed and will direct you to click the "finish" button. 

## Setting up Visual Studio Code 

You will, over time, realize your preferences in Visual Studio Code; however, here are the settings we recommend beginning with when starting Collection Builder. 

## Step 1

- Open your Visual Studio Code and scroll down to the gear icon in the bottom left hand corner of the window. 
{% include bootstrap/figure.md img="howto/visualstudio/screenshotgears2copy.png" caption="click gear icon" alt="screen shot of gear icon" class="w-50"%}

- the select the "settings" option. 
{% include bootstrap/figure.md img="howto/visualstudio/screenshotsettings.png" caption="click the settings button" alt="screen shot of the settings button" class="w-50"%}

- Toward the top right-hand corner of the window you will see a file icon, click on it.  
{% include bootstrap/figure.md img="howto/visualstudio/screenshotfile.png" caption="click on this file icon" alt="screen shot of the file icon" class="w-50"%}

- You will be taken to a tab which will contain two curly brackets. Note: if there is any text contained inside of the brackets delete it now, but leave the brackets.
{% include bootstrap/figure.md img="howto/visualstudio/sreenshot.6.png" caption="curly brackets" alt="screen shot of the file icon" class="w-50"%}

- You will then copy and paste this code in between the brackets. This will update your settings to what we believe will work compatibly with Collection Builder's needs. 

{:.alert .alert-success}
"editor.minimap.enabled": false,  
    "editor.wordWrap": "on",  
    "html.format.maxPreserveNewLines": 2,  
    "html.format.wrapLineLength": 0,  
    "editor.codeLens": false,  
    "outline.problems.badges": false,  
    "outline.problems.enabled": false,  
    "outline.problems.colors": false,  
    "problems.decorations.enabled": false,  
    "problems.autoReveal": false  
    
{% include bootstrap/figure.md img="howto/visualstudio/screenshot.7.png" caption="it should look like this" alt="screen shot of pasted text" class="w-50"%}

- Now that you are complete be sure to save your changes before moving on. You have officially *set up* Visual Studio Code. 