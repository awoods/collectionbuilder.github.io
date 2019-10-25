---
layout: howto
title: How To Install Ruby on Linux
---

[Ruby](https://www.ruby-lang.org/en/){:target="_blank"} is a fairly young and developing programming language with some unique features. 
To use Jekyll, **_you do not need to know anything about Ruby_**, but if you are curious, check out [Ruby in 20 minutes](https://www.ruby-lang.org/en/documentation/quickstart/){:target="_blank"}.
Jekyll requires Ruby version 2.4.0 or above (at the time of this writing), plus a few common build tools. 
Check the [Jekyll requirements](https://jekyllrb.com/docs/installation/) for latest details.

On linux distributions there are two main options for installing Ruby: 
use your distro's repositories or use a Ruby version manager. 
Using your repository is *dead easy* (for example on Ubuntu, `sudo apt install ruby-full`), but will likely not be an up-to-date version of Ruby.
We suggest using [RVM](http://rvm.io/){:target="_blank"} instead.

## Install Build Tools

To install Ruby and Gems (packages for Ruby), you will need some basic build tools (Make and GCC).
Most distributions will have them already installed or will provide a package with everything you will need.
For example, on Ubuntu use `sudo apt install build-essential` to make sure you have everything.

## Install Ruby Using RVM

[RVM](http://rvm.io/){:target="_blank"} is a Ruby version manager, that allows you to install and switch between multiple Ruby versions. 
For the purposes of Jekyll, you will likely only need one Ruby version installed, however, RVM will simplify installing and updating the latest versions. 

https://evanwill.github.io/_drafts/notes/ruby-notes.html

## Alternatively - Install Ruby Using Repo

Even though the version will not be the most up-to-date, the simplest method is to use your distro's repositories. 
For example, on Ubuntu `sudo apt install ruby-full build-essential zlib1g-dev`, or Fedora `sudo dnf install ruby ruby-devel @development-tools`. 
However, you will want to avoid installing Gems as root user--see the official Jekyll [Ubuntu install docs](https://jekyllrb.com/docs/installation/ubuntu/){:target="_blank"} for details of a work around.
