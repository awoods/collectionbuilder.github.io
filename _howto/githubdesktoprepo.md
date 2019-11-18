---
layout: howto
title: How To Set Up the CollectionBuilder Repository in GitHub Desktop
---

{:.alert .alert-warning}
You should already have a GitHub account before proceeding with this How To. You should also have [GitHub desktop](githubdesktop.html){:target="_blank"} and a text editor such as [Visual Studio Code](visualstudiocode.html){:target="_blank"} or [Atom](installatom.html){:target="_blank"}installed your computer.


### Step 1: Create a New Repository in GitHub online

First, you need to [set up a new repository](setupgithubrepo.html){:target="_blank"} on GitHub online for your CollectionBuilder project. Make sure to check the box next to "Initialize this repository with a README." Also there will be a dropdown list button saying "Add .gitignore" under the README checkbox. Click the dropdown, start typing "Jekyll" in the search, and select the "Jekyll" option.

### Step 2: Clone your New Repository

Now that you have a repository set up on GitHub, we need to copy, or [clone](clonegithubrepo.html){:target="_blank"} that folder down to your local machine. It is important to realize that the repository really is just a folder of files! You can open, move, or edit it just like any other folder on your computer.

### Step 3: Download a CollectionBuilder Code Files

Now, you need to get a copy of the CollectionBuilder code.

Click here to download our latest release:

{% include bootstrap/button.md text="CollectionBuilder-CONTENTdm v1.0" link="https://github.com/CollectionBuilder/collectionbuilder-contentdm/archive/v1.0.zip" color="success" %}

{:.py-4 .mt-4 #create}

### Step 4: Add CollectionBuilder Files

- In the bar at the top of your GitHub Desktop window, click on “Repository,” then click on “Show in Explorer” (if you’re on a PC) or “Open in Finder” (if you’re on a Mac). This will show you the location of the repository you just cloned to your computer.
{% include bootstrap/figure.md img="/howto/github/github_repository-showinexplorer.png" caption="Locating the files from your new repository" alt="a screenshot of locating the new repository folder from GitHub desktop" %}
- Locate the .zip folder you downloaded in step 1. 
{% include bootstrap/figure.md img="/howto/github/github_locatingzipfiles.png" caption="Locating the files from the .zip folder" alt="a screenshot of locating the .zip folder" %}
- Extract the files from the .zip folder so you can use them.
{% include bootstrap/figure.md img="/howto/github/github_unzipcontent.png" caption="Extract the files from the .zip folder" alt="a screenshot of how to extract files from .zip" %}
- Go into the folder you extracted and copy all the files within the CollectionBuilder folder. Paste these files into your new repository folder.
{% include bootstrap/figure.md img="/howto/github/github_aftercopyandpaste.png" caption="Your repository files should look like this" alt="a screenshot of how your repository files look after copying and pasting from Collection-Builder" %}

{:.alert .alert-danger}
Do not copy and paste the whole folder you downloaded into your new repository. Make sure to copy all of the files from WITHIN that folder.

### Step 5: View the Code

Now you have all of the CollectionBuilder code in your repository! You can now view it and customize it to fit the collection you want to make. But first you need to [commit and push](pushpullchanges.html){:target="_blank"} your changes to GitHub as a sort of way to "save" or "sync" your edits to your online GitHub account.

You can view what changes you made by [generating your site](generatingsite.md){:target="_blank"} in your text editor (like Visual Studio Code).