---
layout: post
title: "In terms of data structures, what is a hash table key?"
description: "Hash Tables are always good to use a quick search."
modified:
categories: java
comments: true
tags: [java, data structures, hash, OOP]
date: 2011-01-21
---
Let me start with the definition of "why Hash Tables good to use”?  

#### Hash Tables are always good to use a quick search.
Let’s suppose we have an array full of data for instance1000 items, and we know exactly what is the index of each item, so we can access it quickly through its index. For example we know the item-abc is located on index 22 so we can apply following:
<br/><br/>
`myItem = myarray[22];`
<br/><br/>
Now, the problem is how we come to know the position of item-abc is 22?<br/>
This is where hashing comes in handy.  

Given some key we can apply a hash function to it to find an index or position that we want to access.  
<br/>
Note: This is an answer of a question on Facebook questions application<br/><br/>
(Source: [facebook.com](https://www.facebook.com/q/In-terms-of-data-structures-what-is-a-hash-table-key))
