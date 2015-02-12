---
layout: post
title: "Grails bind request parameters with command object"
categories: grails
tags: [grails, commandObject, bindData, request]
date: 2014-08-30T22:41:45+04:00
comments: true
share: true
---
When i was working on credit card payment gateway [(Direct Link)](http://www.payfort.com/index.php/en/products/online-card-payment.html#directlink) integration i came across in a situation where i had to bind request parameters with command object however due to weird bug in grails you cannot bind upper case parameters with  command object. I've reported this bug @ [GRAILS-11691](https://jira.grails.org/browse/GRAILS-11691)  
\\
Im my situation payment gateway redirect back to a url of my application with parameters based on those parmeters we decide whether transaction went successful or not. However, the parameters returned by payment gateway were in upper case format i.e. OrderID, Alias, etc etc due to third party involvement i had pretty much no control over parameters case format. Therefore to handle this scenario I wrote following method:

{% highlight groovy linenos %}
/**
 * Method to convert params and populate params map in a format so that params
 * can be bind with command object.s
 *
 * @param params request params map to convert in lower case params
 * @param success true in case request is for success
 *
 * @return map of params
 */
private Map paramsMap(Map params) {
  Map paramsMap = [:]

  paramsMap.orderId = params.OrderID
  paramsMap.status = params.status

  return paramsMap
}
{% endhighlight %}

Then to bind request object with request params in `success` action

{% highlight groovy linenos %}
/**
 * Payment gateway redirect to this action.
 */
def success () {
  CommandObj command = new CommandObj()

  bindData(command, paramsMap(params))

  if (command.validate()) {
    // validation passed proceed with operation
  } else {
    // validation not passed return errors.
  }

}
{% endhighlight %}
