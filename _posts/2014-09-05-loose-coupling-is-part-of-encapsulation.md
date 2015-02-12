---
layout: post
title: "Loose coupling is part of encapsulation?"
description: "Loose Coupling is not a part of encapsulation, coupling use encapsulation, where the well-encapsulation can be achieved without loose coupling."
modified:
categories: java
comments: true
tags: [java, OOP, Encapsulation]
date: 2010-09-27
---
No Coupling is not a part of encapsulation, coupling use encapsulation, where the well-encapsulation can be achieved without loose coupling. For example, I’ve a DSLR Camera(MyCamera) and two lenses of Different types which i switch between quite often as per my photography shoots requirement.<br/><br/>
So lets say I have a Camera MyCamera & having 1 lens to take wide angle pictures and 2nd to take really close photos of any object.<br/><br/>
Check the following code:

{% highlight java %}

interface Lens { }

class MacroLens implements Lens { }

class WideAngleLens implements Lens { }

public class MyCamera{
  private Lens lens;
  MyCamera (Lens lens) {
    this.lens = lens;
  }
}
{% endhighlight %}
The above code demonstrate well-encapsulation + loose coupling with each other. I can switch lenses easily from Wide Angle Lens to Macro Lens. If I were use following code:
{% highlight java %}
public class MyCamera{

private WideAngleLens lens;
  MyCamera(WideAngleLens lens){
    this.lens = lens;
    }

}
{% endhighlight %}

[original post](http://www.coderanch.com/t/511570/java-programmer-SCJP/certification/Benefits-encapsulation#2313782)
