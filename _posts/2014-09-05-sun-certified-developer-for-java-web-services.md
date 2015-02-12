---
layout: post
title: "Passed Java-EE5 WebServices Developer Certified Professional Exam."
description: "My experience while preparing for Java-EE5 WebServices Developer Certified Professional Exam"
categories: java
tags: [java,JavaWebServices, SCDJWS5]
date: 2010-09-16
---
I’ve cleared SCDJWS5 exam today morning with 79%. I’ve been preparing for this exam since more than 4 months there were 65 question & 150 minutes, and I answered 51 questions correct and took 1 hour 30mins. Most of the questions were from SOAP, JAX-WS, Security, WSDL, UDDI & WSI sections where the security related questions were toughest for me among all I got only 40% on this Section.<br/><br/>

#### Following are some points which I observe from my exam questions for the peoples who wish to attempt this exam in future.

+ Remember the communication mode supported by JAX-WS and JAX-WS support for data bindings.
The difference of document-literal & rpc-literal.
- You have to choose the answer carefully of such questions where you asked what can EJB-based Endpoint & Servlet-based Endpoint can access, like EJB endpoints can take advantage of container managed transactions.
- Thoroughly take inside look on xml schemas to define arrays and java primitives types.
- Check the validation-of-schema first if the xml schema provided in question.
- Remember the steps to establish connection with a UDDI registry using JAXR client.
- Svcutil.exe is a utility if DotNet to generate proxies of framework similar like wsimport in java.
- Take a thorough look on SOA+UDDI advantages such as:
  - UDDI provides location where services can be dynamically discovered.
  - Remember SOA is only a way to design a system and Web service is possible implementation, I’ve got two questions related to SOA.
- Remember if the operation is in-only then it cannot send a SOAP fault back to the sender.
- I’ve got 2 questions on interaction layer; check the benefits of interaction layer what they are appropriate for?
- Check the scenario when you want to switch your web service from synchronous Web service interaction to an asynchronous.
- I got one question to choose either SOAP Web Service or RestFull your concept should clear on “what is the appropriate usage in certain situation?”
- Check the Syntax of portType element for request/response or request -only operation in WSDL.
- You should able to decide between java-to-wsdl and wsdl-to-java approach appropriate for certain scenario.
- I got a question on the JAXB data binding steps/process (which I think made wrong)
- And again I forgot SAAJ extends DOM API not SAX API and made one question wrong on it **sigh**
- I’ve got one, one question on each of topic(JAXP, StAX, SAAJ & SAX).
- Try to run each code example given into Ivan’s notes specially regarding security.
- There are great step by step code examples in “Java Web services up & running” book give a try to each of them yourself.  


Furthermore, I had used RMH & Java web services up & running book and always use to open Ivan’s notes pdf side by side when studying those books. It’s very easy to find the each API specification links in this PDF it’s a great resource for preparation.
<br/><br/>
[Original Post](http://www.coderanch.com/t/510426/sr/certification/Passed-SCDJWS-exam-today)
