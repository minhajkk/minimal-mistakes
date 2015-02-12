---
layout: post
title: "Java Encapsulation"
modified: 2014-07-12 14:23:08 +0400
category: java
description: "Encapsulation - One of the four fundamental OOP concepts"
tags: [java,scjp]

comments: true
share: true
date: SEPTEMBER 27, 2010
---

Encapsulation is one of the four fundamental OOP concepts.The ability to make changes in your implementation code without breaking the code of others who use your code is a key benefit of encapsulation.
Let me give you an example:
Lets say you have a class User, which holds User name and password

{% highlight java linenos %}
public class User{
  private String userName;
  private String password;

  public String getUserName(){
    return userName;
  }

  public void setUserName(String uname){
    this.userName = uanem;
  }


  public String getPassword(){
    return password;
  }

  public void setPassword(String pass){
    this.password = pass;
  }
}
{% endhighlight %}

And a lot of other programmers(may be 1000s) wrote programs that used your class such as:

{% highlight java linenos %}
User user = new User;
user.setUserName("theUserName");
{% endhighlight %}

Now your Manager announced some new rules:

1. User name cannot be null.
2. Password cannot be null.
3. No one can set the user name less then 5 characters.
4. No one can set the password less then 5 characters.

Just Think how easy it would be to make above changes by following the encapsulation rules. instead of changing all the code where your `User` class is used you would change only `setUserName(string)` & `setPassword(string)` method as per code listed below.

{% highlight java linenos %}
public void setPassword(String pass){
  //check password is not null;
  //check password is more than 5 character long.
  //set password.
}

public void setUserName(String uname){
  //check user name is not null;
  //check user name is more than 5 character long.
  //set username.
}
{% endhighlight %}

You made the change only at one place and the the other 1000s of programmers code will adopt those rules automatically!!\\
\\
\\
Originally posted @ [link](http://www.coderanch.com/t/504996/java-programmer-SCJP/certification/Encapsulation#2279152)
