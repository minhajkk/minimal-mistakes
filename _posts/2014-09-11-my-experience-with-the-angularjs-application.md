---
layout: post
title: "My Experience with the Angularjs and First hackathon at Cobone"
excerpt: "My experience while preparing for Java-EE5 WebServices Developer Certified Professional Exam"
categories: java
excerpt: "One fine day we (TechOps team at cobone) were rudely shaken from our Ramadan muses during the ramadan as we received an email from the head of IT with the subject PM Application"
tags: [grails, angularjs, hackathon, cobone, triperna]
date: 2014-09-11T20:43:21+04:00
share: false
comments: false
---
<section id="table-of-contents" class="toc">
  <header>
    <h3>Overview</h3>
  </header>
<div id="drawer" markdown="1">
*  Auto generated table of contents
{:toc}
</div>
</section><!-- /#table-of-contents -->
One fine day we (TechOps team at cobone) were rudely shaken from our Ramadan muses during the ramadan as we received an email from the head of IT with the subject **"PM Application"**. Suffice to say we felt like re-enacting the The Social Network film hackathon scene where Mark Zuckerberg messes up with the minds of a couple of dudes in search of an internship; the only interview that combines booze, code, Python, PIX Firewall Emulator and a cheering squad. Our task was not that sick but auspicious enough, perhaps because it was our first hackathon at [Cobone](http://www.cobone.com).
We had to build two applications just to get a hang of new technologies with Angularjs and grails restful API capabilities. We had to develop a project management application with the following specs:  

### Specs:
1. User can register
2. User can login
3. User can create a Project (supports CRUD)
4. Against a project user can add tasks (Supports CRUD)
5. Against a task users can add comments

### Frameworks and tools to be used:
+ Grails
+ AngularJS
+ Yeoman
+ Twitter Bootstrap
+ GIT
+ IntelliJ or Atom or Both

### Bonus:
+ Deploy on Heroku
+ Create an Entity Plugin instead of single Grails project  

Since it was my first experience with the Angularjs framework, you guessed right! I was feeling Morpheus in the Matrix, ready to crack a line of code to change the destiny of the world. However, my heavenly enthusiasm was brought back to the world when I learned it was better to flirt with Ugly Betty than butter up Angularjs. The problem was that with Angularjs, the only examples on the internet were written in a different style with no common solutions for common problems. Everyone seems to have a personal style/standard for messing up with Angularjs. For example, we almost went into an amateur mixed martial arts fight on the structure of Angularjs application, especially after realizing the Yeoman default structure is not very impressive.  
<br/>
Due to time constraint and my limited experience with Angularjs, I could not complete <a href="http://minhajkk.github.io/grails-restful-angular-client/" targe="_blank">frontend</a> (Angularjs) application. But I had to suck up and do something or else I would be lost in a line of code or in an application that seemed to be low on mercy points. What I did was along with the API project, I gave an interface to grails restful app itself.  
<br/>
I began the development of the API Project (I named it grails-restful) and it was all about exploring the grails-restful capabilities. While grails-restful has nothing to do with the Holy Grail I started having some breakthrough and felt like the Hackathon’s big Kahuna. It was a great experience to explore newer version of grails, i.e. 2.4.2, and its amazing support for restful web services. The major challenges I faced during the API Project development were not just confined to missing my bed or desiring coffee coded to perfection. They included:

#### The major challenges i've faced during api project development were.  
- Configuring spring security plugin to provide rest based authentication.
- Cross Domain origin issue To enable cross site AJAX requests.
- Writing grails restful controllers test cases. check the [ProjectControllerSpec](https://github.com/minhajkk/grails-restful/blob/master/test/unit/com/scrum/ProjectControllerSpec.groovy)

I have deployed the grails-restful application on Heroku @ [http://grails-restful.herokuapp.com](http://grails-restful.herokuapp.com).

#### Plugins i used for grails restful project.<br/>
- [Spring Security Core](http://grails.org/plugin/spring-security-core)
- [Spring Security Rest](http://grails.org/plugin/spring-security-rest) For providing rest  based security (I <span class="fa fa-heart"/> this plugin)
- [Twitter-bootstrap](http://grails.org/plugin/twitter-bootstrap)
- [Asset-pipeline](http://grails.org/plugin/asset-pipeline)
- [MongoDb](http://grails.org/plugin/mongodb)
- [Cors](http://grails.org/plugin/cors) To enable cross site AJAX requests
- [Coveralls](http://grails.org/plugin/coveralls) For using coveralls.io
- [Code Coverage](http://grails.org/plugin/code-coverage) For codecoverage

#### The application consist of basically 4 parts  

1. Register/Login
<figure class="half"><a href="/images/grails-restful-app/register-login.gif"><img src="/images/grails-restful-app/register-login.gif"></a></figure>
2. Create/Delete Project
<figure class="half"><a href="/images/grails-restful-app/projects-index.gif"><img src="/images/grails-restful-app/projects-index.gif"></a><a href="/images/grails-restful-app/create-project.gif"><img src="/images/grails-restful-app/create-project.gif"></a></figure>
3. Create/Delete Tasks
<figure class="half"><a href="/images/grails-restful-app/create-task.gif"><img src="/images/grails-restful-app/create-task.gif"></a></figure>
4. Add comments
<figure class="half"><a href="/images/grails-restful-app/add-comments.gif"><img src="/images/grails-restful-app/add-comments.gif"></a></figure>

#### Plugins used for deployment at Heroku include:
- [heroku](http://grails.org/plugin/heroku)
- [cloud-support](http://grails.org/plugin/cloud-support/)

#### The source code for grails-restful application can be found @github:
+ grails-restful [https://github.com/minhajkk/grails-restful](https://github.com/minhajkk/grails-restful)
+ client app [https://github.com/minhajkk/grails-restful-angular-client](https://github.com/minhajkk/grails-restful-angular-client)
+ Entities plugin [https://github.com/minhajkk/entities/](https://github.com/minhajkk/entities/)

Angularjs and Heroku or not, I feel like I could take Zuckerberg and his shot-taking fellowship of internship seekers. I feel like Python already.
