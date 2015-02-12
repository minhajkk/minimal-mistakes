---
layout: post
title: "Google pageviews tracking with spring/grails flows"
modified: 2014-07-13 22:38:48 +0400
category: grails
tags: [grails]
image:
  feature:
  credit:
  creditlink:
comments: true
share: true
date: MAY 26, 2013
---
If you’re working with spring/grails flows!! tracking page views of each step of flow as different url with google analytics could be real a pain.
<br/><br/>
However to succeed in dealing with this issue use `_trackPageview` method along with a URL in order to track different url than original(in address bar). e.g.
{% highlight javascript %}
_gaq.push(['_trackPageview', '/checkout/step1']);
{% endhighlight %}
Instead of
<br/>
{% highlight javascript %}
_gaq.push(['_trackPageview']);
{% endhighlight %}
