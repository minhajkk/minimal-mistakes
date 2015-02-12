---
layout: post
title: "Why a class declare as abstract if it does not have any abstract method"
modified: 2014-08-06 23:15:00 +0400
category: java
description: "Abstraction - One of the four fundamental OOP concepts"
tags: [java]
image:
  feature:
  credit:
  creditlink:
comments: true
share: true
date: 2010-08-04
---
#Java Abstract classes#

Well, we declare a class abstract when we want to give some ready made behaviour to a child, the child will have choice to override their own behavior or just simply inherit from father, this is something that we cannot achieve with Interfaces.
<br /><br/>
Lets say: We have a Father class Animal for all the animals following listed two behaviour of an animal.

1. fly.
2. sound.

Each Animal can sound, but only bird animals can fly...

Check out the following example.
{% highlight java linenos %}
abstract class Animal{

  //only the birds are able to fly…
  public void fly(){
    System.out.println("Only the birds can fly...");
  }

  //every animal sounds different.
  abstract public void sound();
}

class Cat extends Animal{

  //A cat cannot fly.

  public void sound(){
    System.out.println("Meaooww...!!");
  }
}

class Duck extends Animal{

  //A Duck can fly...so implement their fly behaviour.
  public void fly(){
    System.out.println("See...Ducks can fly");
  }

  public void sound(){
    System.out.println("Quack Quack!!");
  }

}

public class Main{
  public static void main(String... args){
    Cat cat = new Cat();
    cat.fly();
    cat.sound();

    Duck duck = new Duck();
    duck.fly();
    duck.sound();
  }
}
{% endhighlight %}

Abstract class is just like a concept where its child classes are the real things. Similarly Animal itself is not something that exist in real, the Animal cat,duck, dog and so on are real objects…
<br/><br/>
Therefore, Animal class in above example is an abstract because animal is no more than a concept no one can create an object of Animal in reality Cats, Dogs, Ducks, and etc exists…
<br/><br/>
Originaly posted on coderacnh.com @ <a href="http://www.coderanch.com/t/505357/java-programmer-SCJP/certification/class-declared-Abstract-abstract-method#2281011" target="_blank">this link</a>
