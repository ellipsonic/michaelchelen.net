---
layout: article
uuid: 651f1da1-9c42-49bb-9001-be7b8f99b56d
title: Blogging with Git using Jekyll on Ubuntu 11.10
name: blogging-with-git-using-jekyll-on-ubuntu-11-10
created_at: 2011-11-13
updated_at: 2011-11-13
categories: unfinished git jekyll ruby ubuntu
---


Jekyll website generator that is compatible with Git version control. The template system can be configured for a blog style layout. The static website files can then be served by any standard webserver.


## Client System ##

This is the system where you will be doing the editing, usually your desktop.
   
    
## Install Dependencies ##
These are required for proper compilation of Ruby.

    sudo apt-get install build-essential openssl libreadline6 libreadline6-dev curl git-core zlib1g zlib1g-dev libssl-dev libyaml-dev libsqlite3-0 libsqlite3-dev sqlite3 libxml2-dev libxslt-dev autoconf libc6-dev ncurses-dev automake libtool bison subversion

    
## Install RVM ##
For installation of the latest version of Ruby on Ubuntu we will use RVM, the [Ruby Version Manager](http://beginrescueend.com/).

We need a more recent version of Ruby because an error exists between directory_watcher and RubyGems 1.3.7 which can be fixed by using a version later than 1.8.6. 

https://github.com/TwP/directory_watcher/issues/10#issuecomment-2327743

The Ubuntu package `ruby-rvm` might also work but doesn't include as recent a version of RVM.

    bash < <(curl -s https://raw.github.com/wayneeseguin/rvm/master/binscripts/rvm-installer)

# install ruby
    rvm install ruby-1.9.3

# select version to use
    rvm use ruby-1.9.3

# test
    ruby -v


# install jekyll
gem install jekyll --no-rdoc --no-ri

    
## Recommended ##    


# faster lsi
gem install gsl

sudo apt-get install libgsl-ruby

# markdown support
gem install rdiscount

    
    
sources:
https://rvm.beginrescueend.com/rvm/install/




with rvm sudo should not be used to install gems

http://beginrescueend.com/rubies/rubygems/





