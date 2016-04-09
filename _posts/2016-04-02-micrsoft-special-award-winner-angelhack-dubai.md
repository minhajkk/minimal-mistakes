---
layout: post
title: "Ionic framework and Microsoft Emotion API "
modified:
categories: 
excerpt:
tags: [hackathon, dubai-internet-city, selfielyzer, microsoft, ionic, project-oxford]
image:
  feature: /Micrsoft-Special-Award-Winner/landing.png
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

A week ago <a href="http://www.hackathon.io/angelhack-dubai1" target="_blank">AngelHack Dubai 2016 hackathon</a> went down between 1st and 2nd April where I join Selfielyzer idea.

## Selfielyzer
<a href="http://www.hackathon.io/selfielyzer" target="_blank">Selfielyzer app</a> happened to be all about selfies and emojis as we worked to create an Artificial inteligence app known as Selfielyzer, a very unique technology that’s not just pretty but the funniest way of replying to posts from your friends and family. Think of vanity with real-life emojis.

Selfielyzer essentially tells you about the content you've shared, from writings, video and picture through selfie feedback using <a href="https://www.microsoft.com/cognitive-services/en-us/emotion-api" target="_blank">Microsoft's emotion API</a>. It was an understanding you can engage with anyone emotionally and as you share posts with friends, family and fans, you get to know what the content you've shared make them feel. Your brand image is put into the test of human eyes and interaction and selfie feedback from them lets you know the feeling the posts make them feeling, whether you are totally awesome, a jerk, happy or anything in between. 

## Tech Stack

Selfielyzer is an ionic framework based hybird app which uses <a href="https://www.microsoft.com/cognitive-services/en-us/emotion-api" target="_blank">Microsoft's emotion API</a> for extracting emotions from selfie image. Source code is available open source @ <a href="https://github.com/minhajkk/selfielyzer">https://github.com/minhajkk/selfielyzer</a>

#### Project Structure

{% highlight text %}
├── wwww (angularjs client side app)
│   ├── css 
│   ├── img
│   ├── js (angularjs services/controllers sciprts)
│   ├── views (views folder)
|   └── index.html (main screen)
├── bower.json (client side dependencies)
└── package.json (server side dependencies)
{% endhighlight %}

#### Screenshot

<figure class="third">
    <a href="/images/Micrsoft-Special-Award-Winner/1.png"><img src="/images/Micrsoft-Special-Award-Winner/1.png"></a>
    <a href="/images/Micrsoft-Special-Award-Winner/2.png"><img src="/images/Micrsoft-Special-Award-Winner/2.png"></a>
    <a href="/images/Micrsoft-Special-Award-Winner/3.png"><img src="/images/Micrsoft-Special-Award-Winner/3.png"></a>
    <a href="/images/Micrsoft-Special-Award-Winner/4.png"><img src="/images/Micrsoft-Special-Award-Winner/4.png"></a>
    <a href="/images/Micrsoft-Special-Award-Winner/5.png"><img src="/images/Micrsoft-Special-Award-Winner/5.png"></a>
    <figcaption>Selfielyzer app screenshots</figcaption>
</figure>

## Microsoft Emotion API

Microsoft's Emotion API allows you to build more personalized apps with Microsoft’s cutting edge cloud-based emotion recognition algorithm. API takes an image as an input, and returns a set of emotions for each face in the image, as well as bounding box for the face, from the Face API. The emotions detected are happiness, sadness, surprise, anger, fear, contempt, disgust or neutral.


## Challenges Faced

<a href="https://dev.projectoxford.ai/docs/services/5639d931ca73072154c1ce89/operations/563b31ea778daf121cc3a5fa" target="_blank">Microsoft's API</a> is fairly simple to use the only thing that took me long to figure out is converting base64 image to raw data and pass it to API in post request body, thanks to one of microsoft tech evanglist who come to resuce and shared <a href="https://social.msdn.microsoft.com/Forums/sqlserver/en-US/807ee18d-45e5-410b-a339-c8dcb3bfa25b/testing-project-oxford-ocr-how-to-use-a-local-file-in-base64-for-example" target="_blank">this</a> code example for converting base64 image into raw format.

## What's next?

- Convert selfie into emoji.
- Add watermarking on generated image.
- Add social share to share selfielyze picture.

## Microsoft Special Award

As Microsoft special award winner, Selfielyzer won:

- Interview with Microsoft Gulf HR
- 1:1 Office Hours with Microsoft Technical Evangelist
- For the team, BizSpark nomination which includes 3 years of FREE software, services, tech support, and upto $750 credit in Azure cloud.

## Links
- <a href="https://www.microsoft.com/cognitive-services/en-us/emotion-api/documentation">Microsoft Emotion API</a>
- <a href="http://angelhack.com/2016/04/05/angelhack-dubai-compareit4me/">compareit4me’s tech evangelist smashes it at Angelhack Dubai 2016!</a>