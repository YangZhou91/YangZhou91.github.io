---
layout: post
title: "Tencent Code Star (Season 1)"
description: "This is a walking through of Tencent Code Star"
category: Web, Front End, Web Knowledge, Problem Solving
tags: [intro, tutorial, note]

---
{% include JB/setup %}

This is my practice of Season 1 game, I hope I will have fun and learn something. This is really the first time to solve this kind of puzzle.

## My Speech

This is Mar 16, 2014. The Season 2 competion of the Tencent Code Star is about to release in 4 to 5 days. I got two midterms this week and a Micro P lab demo!! I have to teach myself about recommender system and submit my first result by Saturday midnight. Can not imagine the life before graduating in one year. 

Anyway, I have to start to earn some credits for the furture job.

## Overview

This the Season one of the Code Star. From my understanding, this about the front-end of trouble shooting and problem solving skills of Web. It can be tell from the organizer of the game. It is called Tencent Alloy Team(腾讯Web前端团队).

## Walking through

Here is the link to the <a href = "http://codestar.alloyteam.com/q1/">game page</a>.

### Step 1

![Step 1]({{site.url}}/assets/2014-03-16-tencent-code-star/ScreenShot2014-03-16at9.14.19PM.png)
I receieved an email from my boss, asking me to spy a new product from TX. I might come from 360? 周鸿祎躺枪～

It was funny to see that my company actually use qq's mail service but against Tencent.

### Step 2

![Step 2]({{site.url}}/assets/2014-03-16-tencent-code-star/ScreenShot2014-03-16at9.27.21PM.png)
So, I went to Tencent HeadCourt and found a breaking point of their building, with tears..

Then click the blue button, and go.

### Step 3
![Step 3_1]({{site.url}}/assets/2014-03-16-tencent-code-star/ScreenShot2014-03-16at9.34.59PM.png)
I was asked to enter my name and email address. I need those to break into a phyical building. Whatever...

![Step 3_2]({{site.url}}/assets/2014-03-16-tencent-code-star/ScreenShot2014-03-16at9.38.09PM.png)
Then I got an error of js pop-up window say error, "Could not open it, and check the communcation." This gave me a hint of checking get and post method of http protocol. I had experience from the write an auto-buyer for the FIFA Ultimate Team. I choose to use the Fiddler plug-in for Chrome(Don't really have many chooses on the Mac OS). OK, this is a wrong approach. I could not read the post request for some reason. 

Then I found something by inspecting the source page. From the built-in developer tool, I got the following info. 
![Step 3_3]({{site.url}}/assets/2014-03-16-tencent-code-star/ScreenShot2014-03-16at9.53.07PM.png)
There was a field named timestamp with attribute of hidden. If I change the 'hidden' to be 'text', there would be another row showing at the bottom.
![Step 3_3]({{site.url}}/assets/2014-03-16-tencent-code-star/ScreenShot2014-03-16at10.06.31PM.png)
Let's try something stupid to test invalid inputs.


