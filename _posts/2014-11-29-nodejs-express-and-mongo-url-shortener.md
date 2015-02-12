---
layout: post
title: "The Place of Node.js, Express and Mongo Technologies Today"
modified:
category: nodejs
categories: nodejs
excerpt: The world today is all about social and collaborative applications and having an easy deploy and built backend is way important.
tags: [nodejs]
image:
  feature:
date: 2014-11-29T03:34:13+04:00
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
The world today is all about social and collaborative applications and having an easy deploy and built backend is way important. Lots of organizations today are relying on an app stack through a number of technologies such as MongoDB, Express and Node.js. It is a stack that has become a favourite for many, especially in mobile apps due to the fact that the native information format is essentially JSON and can be parsed easily by applications through comparable parsers In fact, a great yet simple app such as <a href="https://github.com/minhajkk/nodejs-url-shortener" target="_blank">nodejs-url-shortener</a> has been created through these vital technologies. 

### Node.js
I think lots of java developers (instead I would say backend developers) are not very comfortable with Javascript including me or understand it well although it is a very common language in the world of web development. 

Node has become globally popular as an ideal web framework as much as there are lots of reasons why it is a good back-end service in many respects. Node has V8, a rapid javascript engine, server functionality (in built), a programming event driven asynchronous model and great dependency management via npm(node package manager). At the same time, MongoDB and Node.js are generally scalable and easily synchronized via a number of machines within a model of distribution. The combination is a wonderful choice for apps lacking a load that is distributed evenly.

### Express
A popular module of Node.js, Express is very important in routing middleware. This separate package is vital for many reasons. For instance, if one ends up using "http" alone or by itself, the location's request would have to be parsed separately towards figuring out the content that need to be served up to a caller, something that becomes impossible in  just a short period. With Express on the other hand, routes can be easily defined including callback chains for every request. Through Express it is also easy for diverse callbacks to be provided as per a certain http verb such as HEAD, DELETE, and PUT or POST among others. 

### MongoDB
JSON objects are stored in a MongoDB database. It contrasts with SQL Database in that as one of the NoSQL databases, Mongo hardly supports relationships among entities. Also, a predefined schema is absent and entities with the same table or collection hardly require similar fields or conforming to a particular predefined pattern. At the same time, MongoDB comes with a strong querying language known as <a href="http://docs.mongodb.org/manual/core/map-reduce/" target="_blank">Map-reduce</a> together with location data support. Due to its ability to shared, replicate and scale, MongoDB is very popular. Rather than storing JSON as it is, MongDB stores it in a BSON format (Binary JSON), which is highly efficient for queries and storage of data. BSON comes with more benefits in that it is able to support lots of datatypes more than what JSON does, for instance C-types and dates.

Checkout the MongoDB University free online courses on their <a href="https://university.mongodb.com/" target="_blank">website</a> they are doing amazing job, I’ve learnt many things about NoSql & MongoDB during my online <a href="/images/M101J-Certificate.pdf">M101J</a> course, its a great way to learn MongoDB.

### Url Shortener
* The source code of node url shortener on github @ [https://github.com/minhajkk/nodejs-url-shortener](https://github.com/minhajkk/nodejs-url-)
* This is my attempt to convert url-shortener using yoeman full stack generator [https://github.com/minhajkk/full-stack-url-shortener](https://github.com/minhajkk/full-stack-url-shortener)

### Heroku
* The code is deployed on heroku @ [https://node-us.herokuapp.com/](https://node-us.herokuapp.com/) & [http://mean-shortener.herokuapp.com/](http://mean-shortener.herokuapp.com/)
* There's a great article posted on heroku dev center on step by step deployment of nodejs application at heroku have a look @ [https://devcenter.heroku.com/articles/getting-started-with-nodejs](https://devcenter.heroku.com/articles/getting-started-with-nodejs)