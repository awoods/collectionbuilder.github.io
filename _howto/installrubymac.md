---
layout: howto
title: How To Install Ruby on a Mac
---

[Ruby](https://www.ruby-lang.org/en/){:target="_blank"} is a fairly young and developing programming language with some unique features. 
To use Jekyll, ***you do not need to know anything about Ruby***, but if you are curious, check out [Ruby in 20 minutes](https://www.ruby-lang.org/en/documentation/quickstart/){:target="_blank"}.

{:.alert .alert-warning}
Installing Ruby on Mac can be a PAIN IN THE ASS. Stick with it! We detail several different trouble shooting techniques below, but if you run into other issues, please let us know and we can update this guide with more warnings and (hopefully) solutions. Also, make sure to follow steps 1 and 2!

1. Make yourself a beverage of some sort, adult or otherwise. We recommend a [Terminal Gravity Eagle Cap IPA](https://terminalgravitybrewing.com/eagle-cap) if you're in the Northwest, or a [Bell's Two Hearted](http://www.bellsbeer.com/beer/year-round/two-hearted-ale) if in the East or Midwest. Alternatively, a nice Kombucha or green tea would be excellent as well.

2. Put on something soothing, maybe some [Satie](https://youtu.be/_fuIMye31Gw). 

3. Start with RVM, and good luck. 


Frustratingly, different versions have many dependency and incompatibility problems.
Because of these issues, many use Ruby Managers, such as [RVM](http://rvm.io/){:target="_blank"}, to install and switch between versions.
However, if you are just interested in working with Jekyll, using an installer for your OS should work well.
Jekyll requires a Ruby version that is greater than 2.2.5.

- **Mac:** OS X has a version of Ruby installed by default. Check the version with `ruby -v`. If it is > 2.2.5 you can use the system Ruby, but recommended practice is to set up a separate Ruby development environment. To do this, follow the instructions below, which outline the steps to install Ruby using [Ruby Version Manager (RVM)](https://rvm.io/){:target="_blank"}. Alternatively, some people have success using [Homebrew](https://brew.sh/){:target="_blank"} (`brew install ruby`) or another manager such as [rbenv](https://github.com/rbenv/rbenv){:target="_blank"}, but our experience suggests RVM is best option.
    - Ensure you have Xcode Command Line Tools, if not use `xcode-select --install` to start the installer.
    - Install [Ruby Version Manager (RVM)](https://rvm.io/){:target="_blank"} following the steps below:
        - Install gpg2, using [Homebrew](https://brew.sh/){:target="_blank"}: `brew install gnupg`
        - Get the public key from [https://rvm.io/rvm/install](https://rvm.io/rvm/install){:target="_blank"}: `gpg --keyserver hkp://pool.sks-keyservers.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB`
        - Get the helper script and install RVM stable with ruby: `\curl -sSL https://get.rvm.io | bash -s stable --ruby`
    - Install recent stable version of Ruby:
        - Check [Ruby Downloads](https://www.ruby-lang.org/en/downloads/){:target="_blank"} for number of "current stable version", currently 2.6.4
        - Use RVM to install that version: `rvm install 2.6.4` (this may take a long time...)
        - Set it as default Ruby: `rvm --default use 2.6.4`
        - Check: `ruby -v`