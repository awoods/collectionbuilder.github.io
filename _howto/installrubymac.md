---
layout: howto
title: How To Install Ruby on a Mac
---

[Ruby](https://www.ruby-lang.org/en/){:target="_blank"} is a fairly young and developing programming language with some unique features. 
To use Jekyll, ***you do not need to know anything about Ruby***, but if you are curious, check out [Ruby in 20 minutes](https://www.ruby-lang.org/en/documentation/quickstart/){:target="_blank"}.
Jekyll requires Ruby version 2.4.0 or above (at the time of this writing), plus a few common build tools. 
Check the [Jekyll requirements](https://jekyllrb.com/docs/installation/) for latest details.

{:.alert .alert-warning}
Installing Ruby on Mac can be a PAIN IN THE ASS. Stick with it! We detail several different trouble shooting techniques below, but if you run into other issues, please let us know and we can update this guide with more warnings and (hopefully) solutions. Also, make sure to follow steps 1 and 2!

1. Make yourself a beverage of some sort, adult or otherwise. We recommend a [Terminal Gravity Eagle Cap IPA](https://terminalgravitybrewing.com/eagle-cap) if you're in the Northwest, or a [Bell's Two Hearted](http://www.bellsbeer.com/beer/year-round/two-hearted-ale) if in the East or Midwest. Alternatively, a nice Kombucha or green tea would be excellent as well.

2. Put on something soothing, maybe some [Satie](https://youtu.be/_fuIMye31Gw). 

3. Start with RBenv, and good luck. 

{:.alert .alert-info}
The official [Jekyll install on mac docs](https://jekyllrb.com/docs/installation/macos/) can also lead you through ways of installing Ruby, but the below are currently more accurate and detailed.

Frustratingly, different versions of Ruby have many dependency and incompatibility problems. We've detailed two different ways to install and manage versions on the Mac below. This is necessary, because most Macs come with an older version of Ruby already installed on the OS, but Jekyll and other applications require newer versions to work correctly. 

- Your first step is to Check and see what version your Mac has installed by default. Enter `ruby -v` into your terminal (which you can open by clicking `Command (⌘) + Spacebar`). 
- If the Ruby Version is > 2.2.5 you can use the system Ruby, but recommended practice is to set up a separate Ruby development environment. To do this, follow the instructions below, which outline the steps to install Ruby using [rbenv](https://github.com/rbenv/rbenv){:target="_blank"}. Alternatively, some people have success using [Homebrew](https://brew.sh/){:target="_blank"} (`brew install ruby`) or another manager such as [rbenv](https://rvm.io){:target="_blank"}, but our experience suggests rbenv is currently the best option.

## Get the Command Line Tools First
    - Ensure you have Xcode Command Line Tools, so that you can work with Ruby (and Git, etc.) 
    - Enter `xcode-select --install` to start the installer. Note: this may take some time.
 
## Using rbenv to Install Ruby

- You'll need to use homebrew to install rbenv, you can go to the [Homebrew](https://brew.sh/){:target="_blank"} site and follow their instructions, or follow along below
    - Open your terminal by hitting `Command (⌘) + Spacebar`
    - Once inside your terminal, copy the following, paste it into the prompt and push enter: `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)`
    - Once that finishes, copy and paste `brew install rbenv` into your terminal prompt.
    - Now copy and paste (or write) `rbenv init` into the prompt.
- You'll now need to edit your bash profile so that this setting is constant from now on.  After entering `rbenv init` into the prompt, the terminal will list some text that has instructions you have to follow. On mac it should say to add `eval "$(rbenv init -)` to your bash_profile. To do this, follow the instructions below: 
    - Open your bash profile with the terminal's text editor, nano, by entering  `nano ~/.bash_profile` into the prompt (init will give you the correct filename; if it's different than this, enter it after '~/.')
    - Add `eval "$(rbenv init -)` at the end of the profile when it opens in the screen. 
    - Click `control (^) + X` to exit and save the profile. When prompted whether you want to save the profile, push `y`. 
- Now you're ready to install Ruby!
    - Install the latest version of ruby by copy/pasting or writing, `rbenv install 2.6.3`  (2.6.3 is the latest solid version as of this writing; if you are reading this past August 2020, you may need to check the "Stable Releases" section on [the download Ruby page](https://www.ruby-lang.org/en/downloads/){target="_blank}
    - Now let's set that version as your global Ruby version by entering `rbenv global 2.6.3` into the prompt. 
    - Finally, we're going to rehash, just to be safe: enter `rbenv rehash` into your prompt
- Now let's see if that worked. 
    - Close your terminal and then reopen it by clicking `Command (⌘) + Spacebar`
    - Enter `ruby -v` into the terminal
    - If your terminal indicates that you have Ruby 2.6.3 or higher installed, you've done it!
{:text-success}
Your computer should be using ruby version 2.6.3 now. 

If the installation did not work, you might try using RVM below or googling any error message or other hinderance you encountered. 

## Using RVM to Install Ruby
 - Install [Ruby Version Manager (RVM)](https://rvm.io/){:target="_blank"} following the steps below:
        - Install gpg2, using [Homebrew](https://brew.sh/){:target="_blank"}: `brew install gnupg`
        - Get the public key from [https://rvm.io/rvm/install](https://rvm.io/rvm/install){:target="_blank"}: `gpg --keyserver hkp://pool.sks-keyservers.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB`
        - Get the helper script and install RVM stable with ruby: `\curl -sSL https://get.rvm.io | bash -s stable --ruby`

{:.alert .alert-warning}
We have had a lot of issues recently with the public key from gpg not working. Installations on several computers have been held up at this step. This is why we are currently recommending you use rbenv (above) instead.

    - Install recent stable version of Ruby:
        - Check [Ruby Downloads](https://www.ruby-lang.org/en/downloads/){:target="_blank"} for number of "current stable version", currently 2.6.4
        - Use RVM to install that version: `rvm install 2.6.4` (this may take a long time...)
        - Set it as default Ruby: `rvm --default use 2.6.4`
        - Check: `ruby -v`