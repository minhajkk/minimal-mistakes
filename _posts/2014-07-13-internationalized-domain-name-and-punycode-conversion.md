---
layout: post
title: "Internationalized domain name and punycode conversion"
modified: 2014-07-13 22:55:39 +0400
category: internet
tags: []
image:
  feature:
  credit:
  creditlink:
comments: true
share: true
date: FEBRUARY 16, 2011

---
Few days ago I’ve faced issue with domain which contains special characters such as www.schönesdresden.de. As of may-2010 it’s allowed to have top level domains in international language (e.g http://JP納豆.例.jp).

\\
However, my task was to download the html using [apache httpclient](http://hc.apache.org/httpclient-3.x/) API therefore I have to use `HttpGet(URI uri)` class where-as `java.net.URI` could be any string which follows RFC 2396 rules (In short the domain names other than English are not considerable as valid URI) and finally I came across to following solution after couple of minutes searching on Google.

>  <a href="http://weblogs.java.net/blog/2007/03/29/international-domain-names">http://weblogs.java.net/blog/2007/03/29/international-domain-names</a>

Basically first we have to convert the international domain name into ASCII Compatible Encoding (ACE) to pass it to `HttpGet(URI uri)` class for this purpose Java SE 6 provides an interesting new class: `java.net.IDN` It’s small, simple…very focused on a single task. That task has two parts:

* To convert domain names from practically any Unicode character to an ASCII Compatible Encoding or ACE.
* To convert ACE names back into their full Unicode UTF-16 encoding The toASCII method converts its non-ASCII Unicode characters to an ACE form using an algorithm called punycode.

#### For more details about punyode conversion check [wikipedia link](http://en.wikipedia.org/wiki/Punycode) ####
