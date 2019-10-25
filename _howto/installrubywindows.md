---
layout: howto
title: How To Install Ruby on Windows
---

[Ruby](https://www.ruby-lang.org/en/){:target="_blank"} is a fairly young and developing programming language with some unique features. 
To use Jekyll, ***you do not need to know anything about Ruby***, but if you are curious, check out [Ruby in 20 minutes](https://www.ruby-lang.org/en/documentation/quickstart/){:target="_blank"}.
Jekyll requires Ruby version 2.4.0 or above (at the time of this writing), plus a few common build tools. 
Check the [Jekyll requirements](https://jekyllrb.com/docs/installation/) for latest details.

{:.alert .alert-success}
Ruby installation on Windows is surprisingly easy for Windows 10 machines. So you're in luck! If you run into specific issues, please let us know and we can update this guide with more warnings and (hopefully) solutions. 

## Install RubyInstaller for Windows.

### Step 1 - Download Ruby Installer

- First, [download](https://rubyinstaller.org/downloads/){:target="_blank"} the suggested stable version "WITH DEVKIT" (as of this writing, Ruby+Devkit 2.6.X (x64)) and double click to install.

{% include bootstrap/figure.md img="/howto/ruby/rubyinstaller-download.png" caption="Download Ruby+Devkit 2.6.5-1 (x64)" alt="a screenshot of the first section of the Ruby Installer website" %}

### Step 2 - Run RubyInstaller 

- Open RubyInstaller by double clicking on the file you just downloaded
- Accept the license. 

{% include bootstrap/figure.md img="/howto/ruby/rubyinstaller-license.png" caption="Accept the license" alt="a screenshot of the first menu of the Ruby Installer program, with the license appearing"%}

- On the next page, click "Install" to install Ruby at the recommended location and let it run. Make sure "Add Ruby executables to your PATH" is checked. (It should be by default.)

{% include bootstrap/figure.md img="/howto/ruby/rubyinstaller-install.png" caption="Click Install" alt="a screenshot of the second section of the Ruby Installer install wizard, with an option for beginning the installation" %}

- Wait for the installation to finish. 

{:.alert .alert-warning}
Installing Ruby on Windows may take several minutes, depending on your machine. During one workshop, we waited ten minutes for all of the files to install. So be patient and let the process run.  

- When the installation is complete, you will get a notification page. **Make sure to check the "Run 'ridk install'..." option** in order to setup MSYs2 development toolchain, then click Finish

{% include bootstrap/figure.md img="/howto/ruby/rubyinstaller-runridk.png" caption="Check the 'Run ridk install' button and click 'Finish'" alt="a screenshot of the finishing section of the Ruby Installer wizard" %}

- Your computer will now open up a terminal window to complete the process. **Just press ENTER** to install the MSYS2 DevKit.

{% include bootstrap/figure.md img="/howto/ruby/rubyinstaller-msys2.png" caption="Press ENTER to install MSYS2" alt="a screenshot of the terminal appearing to install the MSYS2 devkit" %}

- Wait for the installation to finish. Like the ruby installation, this may take several minutes. 
- When the installation is complete, another terminal window will pop up telling you the installation succeeded. 
- Press ENTER one more time and the terminal window will close. 

{:.alert .alert-warning}
Sometimes the MSYS2 installation takes a long time, or gets hung up. Wait for some time, but if it seems to be stuck, close the terminal, then reopen it, using the instructions below on how to open a terminal and type `ridk install` into the command prompt to restart the installation. 

### Step 3 - Check that it Worked!

- Open up a terminal window by typing "terminal" into the Windows search box near the start menu. (If you want to learn more about opening and using the terminal, check out our [How To Open Up the Terminal](openaterminalwindows.html) page)

{% include bootstrap/figure.md img="/howto/ruby/openterminal.png" caption="Type 'terminal' into the search box and open the Command Prompt app" alt="a screenshot of the Windows 10 start screen with 'terminal' written into the search box and command prompt app appearing at the top" %}

- Click to open the "Command Prompt" app that comes up. 
- Type `ruby -v` into the prompt and hit enter. 

{% include bootstrap/figure.md img="/howto/ruby/ruby-v.png" caption="Type `ruby -v` into the command prompt" alt="a screenshot of the terminal with 'ruby -v' typed into the command prompt" %}

- If the terminal lists your ruby version (as in the below), congratulations you've installed ruby!!!

{% include bootstrap/figure.md img="/howto/ruby/rubyversionlisted.png" caption="SUCCESS! Your ruby version is listed. Mine is listed here as '2.5.5'" alt="a screenshot of the terminal after 'ruby -v' has been entered, with ruby version 2.5.5 appearing underneath the prompt" %}

{:.alert .alert-info}
We have had regular success in installing Ruby on Windows using the Ruby Installer. We have, however, mostly been using Windows 10 machines. If you are using an earlier Windows OS, there may be steps or problems we have not encountered. If you have a significant problem with this process, please let us know. We would like to update the documentation for others in the future if any common problems arise. 

{: .pl-4 }
>*<small>Some of this material was gleaned from [an "install ruby on windows" article on stackify](https://stackify.com/install-ruby-on-windows-everything-you-need-to-get-going/).
Check the official [Jekyll install on Windows docs](https://jekyllrb.com/docs/installation/windows/) for more options.</small>*
