---
layout: howto
title: How To Install Ruby on Windows
---

[Ruby](https://www.ruby-lang.org/en/){:target="_blank"} is a fairly young and developing programming language with some unique features. 
To use Jekyll, ***you do not need to know anything about Ruby***, but if you are curious, check out [Ruby in 20 minutes](https://www.ruby-lang.org/en/documentation/quickstart/){:target="_blank"}.

{:.alert .alert-success}
Ruby installation on Windows is surprisingly easy for Windows 10 machines. So you're in luck! If you run into specific issues, please let us know and we can update this guide with more warnings and (hopefully) solutions. 

## Install RubyInstaller for Windows.

### Step 1
First, [download](https://rubyinstaller.org/downloads/){:target="_blank"} the suggested stable version "WITH DEVKIT" (as of this writing, Ruby+Devkit 2.6.X (x64)) and double click to install.

{% include bootstrap/figure.md img="/howto/ruby/rubyinstaller-download.png" class="m-4" caption="Download Ruby+Devkit 2.6.5-1 (x64)" %}

### Step 2
Use the install defaults, but make sure "Add Ruby executables to your PATH" is checked. On the final step, ensure the box to start the MSYS2 DevKit is checked. 

- **Windows:** Use  
    - First, [download](https://rubyinstaller.org/downloads/){:target="_blank"} the suggested stable version "WITH DEVKIT" (as of this writing, Ruby+Devkit 2.6.X (x64)) and double click to install. Use the install defaults, but make sure "Add Ruby executables to your PATH" is checked. On the final step, ensure the box to start the MSYS2 DevKit is checked.
    - Second, the installer will open a terminal window with options to install MSYS2 DevKit components. Choose option 3, "MSYS2 and MINGW development toolchain", or simply press ENTER to install all the necessary dependencies. The installer will proceed through a bunch of steps outputting a bunch of text in the terminal window--*eventually*, this will conclude and you should see a message with success in it. If the window doesn't close, press Enter again or manually close it. (The installer can be restarted by typing `ridk install` into a command prompt)
