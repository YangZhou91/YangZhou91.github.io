---
layout: post
title: "SQLMap notes"
description: "This is a study note got SQLmap tool"
category: Hack, Database
tags: [Hack, Database]
---
{% include JB/setup %}
{{page.date | date_to_string}}

I was recently pissed off by Malaysia, of reaction for MH370. So, my passion towards hacker skills was activated. 

## Overview
I had previous experience BackTrack 5. I was only using Wifi related tools, but there are so many tools I didn't use before. I did a little bit research which turns out the SQLMap is the easist tool to start with. 

sqlmap is an open source penetration testing tool that automates the process of detecting and exploiting SQL injection flaws and taking over of database servers.

## Approach
First of all, we need to find vulnerable website which has some potential for injection. We can simply use google to do this. Google the following words. 
{% highlight Bash shell scripts %}
php?id=1
{% endhighlight %}
Then the google will return the pages with url ends of php?id=1. Those pages are potentially our target. Then randomly choose one page, and go to that page. At the end of url, add ', so you should get something like
{% highlight Bash shell scripts %}
php?id=1'
{% endhighlight %}
Then hit enter, if you find error in the page like following:
{% highlight MySQL%}
SELECT * FROM TABLE WHERE ID=1'
YOU HAVE AN ERROR IN YOUR SQL SYNTAX; 
CHECK THE MANUAL THAT CORRESPONDS TO YOUR MYSQL SERVER VERSION FOR THE RIGHT SYNTAX TO USE NEAR ''' AT LINE 1
{% endhighlight%}
Then it means it has large chance you can use sql injection of this website.

###SQLMap
After you get a potential website, here is where SQLMap comes. Open the command, I have the SQLMap installed already. For detailed installation, go to the SQLMap page. 
{% highlight Bash shell scropts %}
sqlmap -u www.sitename.com/php?id=1 --dbs
{% endhighlight%}

Disclaimer: All the tools and methods described in this tutorial are shown for educational purposes and should not be used for any short of illegal action.
