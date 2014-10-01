---
layout: post
title: "Upgrade Ruby, and Rails with RVM on MacOS"
description: ""
category: 
tags: []
---
{% include JB/setup %}

Operation System: Mavericks -  MacOS 10.9.5 

[RVM](http://rvm.io): installed
[GEM]():installed
## Upgrade Ruby 
First, check the most recent available version of Ruby:
{% highlight bash %}
$ rvm list known
{% endhighlight %}
Then I get a list of Ruby with versions.
{% highlight bash %}
# MRI Rubies
[ruby-]1.8.6[-p420]
[ruby-]1.8.7[-head] # security released on head
[ruby-]1.9.1[-p431]
[ruby-]1.9.2[-p330]
[ruby-]1.9.3[-p547]
[ruby-]2.0.0-p481
[ruby-]2.0.0[-p576]
[ruby-]2.1.2
[ruby-]2.1[.3]
[ruby-]2.1-head
ruby-head
{% endhighlight %}
so, I am goint to update my Ruby to the version '2.1-head' by the following command:
{% highlight bash%}
$ rvm install ruby-<version>
{% endhighlight%}
In my case:
{% highlight bash%}
$ rvm install ruby-2.1-head
{% endhighlight%}

The following message indicate the upgrade is done:
{% highlight bash %}
Install of ruby-2.1-head - #complete
{% endhighlight %}

You may check the version of the Ruby by 
{% highlight bash %}
$ ruby -v
{% endhighlight%}
After upgrade, I have Ruby v2.1.4 installed
{% highlight bash%}
ruby 2.1.4p247 (2014-09-24 revision 47703) [x86_64-darwin13.0]
{% endhighlight%}

## Upgrade Rails by using Gem
To check the version of Rails:
{% highlight bash%}
$ rails -v
{% endhighlight%}
To check the version of Gem:

I have 'Rails 4.0.2' installed. The [Offical Website](http://rubyonrails.org) has Version 4.1 available.
{% highlight bash%}
$ gem -v
{% endhighlight%}
The version of gem is '2.1.11', to update gem manager:
{% highlight bash%}
$ gem update --system
{% endhighlight%}
It takes me to the version 2.4.1

To upgrade the Rails, use the following command:
{% highlight bash%}
$ gem update
{% endhighlight%} 
It takes a while to update all outdated gems. After upgrade, I have Rails with version 4.1.6.

##References: 
1. [Upgrade Ruby Version on Mac OSX](http://techespanto.wordpress.com/2013/03/29/upgrade-ruby-version-on-mac-osx/)

2. [Updating to Rails 4.2](http://railsapps.github.io/updating-rails.html)
