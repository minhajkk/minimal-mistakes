---
layout: post
title: "Real time magic with socketIO"
modified:
comments: true
categories: nodejs
tags: [nodejs, socketio, real time]
image:
  feature: 
date: 2015-05-19T00:08:07+04:00
---
Yo! Last month I've joined <a href="//SellAnyCar.com" target="_blank">SellAnyCar.com</a> my first project at SAC _(along with some other)_ is a real time application based on nodeJS and socketIO framework, its a real time server which helps in real-time bidirectional communication between customer and inspectors.

Since this was my first real time based application I've found socketIO extremely convenient in terms of integration just few lines of code will make an real time application up and running however their documentation is not the best documentation on the face of earth but still good for some initial inspiration <a href="http://socket.io/docs/" target="_blank">http://socket.io/docs/</a> 

### Enuf said
After working on socketIO couple of weeks I was looking for some idea to make an experiment with socketIO and show off my real time skills **:D** so yesterday I decided to add real time support in my first <a href="/nodejs/nodejs-express-and-mongo-url-shortener/" target="_blank">nodejs experiment</a> which is basically an url-shortener application. I've made socketIO integration which updates every client upon new short url creation as shown in bellow screen grab.

<figure>
    <a href="/images/nodejs-url-shortener.gif"><img src="/images/nodejs-url-shortener.gif"></a>
    <figcaption>Real time url shortener</figcaption>
</figure>

The app is deployed on <a href="//node-us.herokuapp.com" target="_blank">heroku</a> (as you can see in above screen grab) and code can be viewed at github @ <a href="https://github.com/minhajkk/nodejs-url-shortener">https://github.com/minhajkk/nodejs-url-shortener</a> 

## Extras
- [How to make your sockets secure?](https://auth0.com/blog/2014/01/15/auth-with-socket-io/)
- [How to send a message to a specific client with socket.io?](http://stackoverflow.com/questions/17476294/how-to-send-a-message-to-a-particular-client-with-socket-io)
- [Dynamic rooms with Socket.io and Node](http://stackoverflow.com/questions/6846174/dynamic-rooms-with-socket-io-and-node)

> Please feel free to use comment box bellow for Any feedback, suggestion or questions? Cheers!