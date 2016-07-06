---
layout: post
title: "Notes of Ruby on Rails"
description: ""
category: [Installation]
tags: [Ruby, Rails]
---
{% include JB/setup %}

Start passenger server with rbenv
{% highlight Ruby %}
	rbenv sudo passenger start -p 80 -e production
{% endhighlight %}

Precompile assets for javascript showing in production environment
{% highlight Ruby%}
	rake assets:precompile
{% endhighlight %}