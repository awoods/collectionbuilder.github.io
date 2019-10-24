---
layout: howto
title: How To Install Ruby on Linux
---

[Ruby](https://www.ruby-lang.org/en/){:target="_blank"} is a fairly young and developing programming language with some unique features. 
To use Jekyll, ***you do not need to know anything about Ruby***, but if you are curious, check out [Ruby in 20 minutes](https://www.ruby-lang.org/en/documentation/quickstart/){:target="_blank"}.


- **Linux:** Even though the version will not be the most up-to-date, the simplest method is to use your distro's repositories. For example on Ubuntu, `sudo apt install ruby-full`. Check `ruby -v` to make sure the repository version is > 2.2.5. See the official Jekyll [Ubuntu install docs](https://jekyllrb.com/docs/installation/ubuntu/){:target="_blank"} for more details.
    - For a more up-to-date version, use a manager such as [RVM](http://rvm.io/){:target="_blank"} ([Ubuntu tips](https://evanwill.github.io/_drafts/notes/ruby-notes.html){:target="_blank"})
    - You will also need some build tools (Make and GCC), on Ubuntu get them with `sudo apt install build-essential`.
