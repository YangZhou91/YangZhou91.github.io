---
layout: post
title: "Recommender System Study Note"
description: "This is a note for learning recommender system from ground."
category: notes
tags: [intro, beginner, tutorial, note]
---
{% include JB/setup %}

This is a note of important points highlighted when I learned about Recommander System. I was about to join the competition 

## Overview

### What is Recommander System?

The Recommander System is envolved some algorithms able to proceed based on huge amount of data, and then determine some possible recommandations based on the browsing history. Those recommandations could be anything related specific their websites or products. For example, the Amazon may recommands some similar books, Youtube may recommands some videos to users.

## Approaches

### Collaborative filtering

This method is based on collecting and analyzing large amount user history data, like browsing，shopping history, then compare to similar users for predicting. The concept is about similar users should have similar preference. A good example should be facebook friends recommandation. If two people shares many mutal friends, then these two should possible know each other.

#### Algorithms 
- Matrix Factroization
- Low-rank Matrix Approximation

### Content-based filtering

This method is based on a description of item or a profile of user's preference. The the system recommends items that are similar to those that a user liked in the past. For example, if a user has a history of buying many non-fiction books, then the algorithm should be able to recommend some related non-fiction books probably with same authers or same topics. The user should not receive recommendation of clothes, or toys.

#### Algorithms
- Bayesian Classifiers
- Cluster Analysis
- Decision Trees
- Artificial Neural Networks  