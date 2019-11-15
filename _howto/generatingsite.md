---
layout: howto
title: How To Generate your Site from Your Text Editor
---
{:.alert .alert-warning}
<div>
    <p>You should already have:
    <ul>
        <li>a text editor such as <a href="visualstudiocode.html" target="_blank">Visual Studio Code</a> or <a href="installatom.html" target="_blank">Atom</a></li>
        <li><a href="installrubywindows.html" target="_blank">Ruby</a> and</li>
        <li><a href="installandupdatejekyll.html" target="_blank">jekyll</a></li>
    </ul> 
    installed for this how-to guide to work for you.</p>
</div>

Generating your website code in your text editor allows you to see your edits as you make them, BEFORE you publish your edits.

### Step 1: Open your Repository in your Text Editor

- View this [guide](openrepointexteditor.html) if you're unsure how to do this.

### Step 2: Open your Terminal in your Text Editor

- View this [guide](openterminalwindows.html) if you're unsure how to do this.

### Step 3: Type `jekyll s` into your terminal

- This is a command working with jekyll to act a local server for your website.
{% include bootstrap/figure.md img="/howto/github/jekylls.png" caption="Locally serving your website" alt="Typing jekyll s into the terminal to locally serve your website" %}

### Step 4: View your Website

- Give it a few seconds and it will generate a link.
{% include bootstrap/figure.md img="/howto/github/jekyllslink.png" caption="Local link for your website" alt="a screenshot of the link for your website" %}

- Hold down the `ctrl` button and click on this link and it will open in your browser.

{:.alert .alert-success}
Now you can see your edits as you make them in your text editor! You don't need to push your changes before viewing them now.

- You will have to save all of your changes and refresh your page before seeing further edits.

### To Stop Serving your Website...

- If you want to serve another website or if you want to close your programs you will have to stop locally serving your website.

- To do this, go back into your terminal and press `ctrl + c`