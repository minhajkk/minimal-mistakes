---
layout: post
title: "NodeJS OCR(Optical character recognition) app"
comments: true
categories: nodejs
excerpt: "Optical character recognition app using tesseract-ocr and nodejs"
tags: [heroku, nodejs, OCR, tesseract]
image:
  feature:
date: 2015-06-27T17:41:35+04:00
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

Mulkiya-OCR is an experiment app, I've used <a href="https://code.google.com/p/tesseract-ocr/wiki/ReadMe" target="_blank">Tesseract</a> Open Source OCR engine to read text from images(for example mulkiya image) so that data input process can be automated and accurate as much as possible. The code is open source at <a href="https://github.com/minhajkk/mulkiya-ocr" target="_blank">github</a>.

> For those who are not familiar with word "Mulkiya". It's an arabic word which means vehicle registration card or vehicle ownership certificate.

## Getting Started
- Install <a href="https://code.google.com/p/tesseract-ocr/wiki/ReadMe" target="_blank">tesseract-ocr</a> open source OCR engine 
- `git clone git@github.com:minhajkk/mulkiya-ocr.git` clone repo from github 
- `npm install` Install the dependencies in the local `node_modules` folder.
- `bower instalk` Install client side bower dependencies.
- `npm start` to run the application.

## Demo
<figure>
    <a href="/images/nodejs-ocr-app.gif"><img src="/images/nodejs-ocr-app.gif"></a>
    <figcaption><a href="https://mulkiya-ocr.herokuapp.com/" target="_blank">https://mulkiya-ocr.herokuapp.com</a></figcaption>
</figure>


## Structure
{% highlight text %}
├── public (angularjs client side app)
│   ├── css 
│   ├── images
│   └── scripts (angularjs services/controllers sciprts)
├── server (nodejs server side app)
│   └── app.js (Entry point to run the application)
|   └── routes.js (routes file)
├── .buildpacks (heroku - installing nodejs/apt/tesseract multiple buildpacks)
├── .gitignore (git ignore)
├── Aptfile (heroku - for installing tesseract-ocr using apt-get)
├── bower.json (client side dependencies)
├── package.json (server side dependencies)
└── Procfile (heroku - process file)
{% endhighlight %}

## Stack
The application is built upon nodejs and angularjs frameworks, find bellow more details about stack.

#### Server Side Dependencies (NPM)
- <a href="https://github.com/expressjs/multer">`multer`</a> Multer is a node.js middleware for handling multipart/form-data.
- <a href="http://expressjs.com/">`expressjs`</a> Web application framework.
- <a href="https://github.com/desmondmorris/node-tesseract">`node-tesseract`</a> A simple wrapper for the Tesseract OCR package for node.js

#### Client Side Dependencies (Bower)
- <a href="https://angularjs.org/">`angularjs`</a> Superheroic JavaScript MVW Framework.
- <a href="https://github.com/angular-ui/ui-router">`ui-routr`</a> For robust routing provider.
- <a href="https://github.com/angular/material">`angular-material`</a> For amazing material design support.
- <a href="https://github.com/danialfarid/ng-file-upload#usage">`ng-file-upload`</a> Amazing angularjs file uploading directive additionally allows mobile devices to capture using camera.

## Deployment
Mulkiya-ocr is deployed on heroku @ <a href="https://mulkiya-ocr.herokuapp.com/">https://mulkiya-ocr.herokuapp.com/</a>. There's a great <a href="https://devcenter.heroku.com/articles/getting-started-with-nodejs#introduction">step by step tutorial</a> provided by heroku for deploying a Node.js app in minutes have a look in case you're interested in using heroku.

Deployment was the main challenge for this application since I had to install `tesseract-ocr` on server before deployment but thanks for heroku's multiple buildpack support It was great experiment using heroku multiple buildpacks on this app. 


## Some useful links
- <a href="https://dDeevcenter.heroku.com/articles/using-multiple-buildpacks-for-an-app">Using Multiple Buildpacks for an App</a>
- <a href="http://challengepost.com/software/heroku-buildpack-tesseract">heroku-buildpack-tesseract</a>
- <a href="http://stackoverflow.com/questions/20034150/implementing-ocr-for-heroku-rails-app">Implementing OCR for Heroku Rails app</a>
- <a href="https://github.com/ddollar/heroku-buildpack-multi">Use multiple buildpacks on your app</a>

## What's next?
1. Manipulate image before processing for example increase/reduce brightness/contrast so text can be extracted easily.
2. Develop algorithm's to extract right information from mulkiya such as model, car, year etc etc
