---
title: 2020 cloud strategy
date: 2019-04-09
thumb_img_path: images/1.jpg
content_img_path: images/1.jpg
excerpt: Looking at the landscape of cloud transformations, three main strategies
  stand out
template: post
subtitle: An exec summary of the state of the art in cloud transformation

---
Looking at the landscape of cloud transformations, three main strategies stand out

## **The cloud-native serverless strategy**

### **For whom?**

For applications that are built cloud-first and that do not mind being wedded to a cloud provider

### **Main benefits?**

#### Benefit #1: write a *lot* less code.

A great Steve Jobs quote from 1997 to illustrate the value of this:

> The way you get programmer productivity is not by increasing the lines of code per programmer per day. That doesn’t work. The way you get programmer productivity is by _eliminating_ lines of code you have to write. The line of code that’s the fastest to write, that never breaks, that doesn’t need maintenance, is the line you never had to write

Leveraging as many as possible of AWS’s new “serverless” services allows to abstract complex pieces of architecture and focus on the business-specific logic. Resulting in apps containing sometimes 10x less lines of code than before.

Some examples of the many game-changing abstractions currently provided by AWS serverless services:

* API gateway for routing
* Cognito for authentication
* Amplify for basic UI building blocks
* SQS to build an event-driven architecture without worrying about the infrastructure required to make it happen
* And my favourite one: step functions to model business workflows in simple functions linked together by a state machine

#### Benefit #2: scaling up. 

Code in serverless is meant to be separated into simple functions run in separate “lambdas”. This forces to architecture the code in a stateless way that makes auto-scalability very easy. It makes scaling up very easy and cost-efficient.

#### Benefit #3: scaling down.

The stateless and on-demand architecture that allows for easy up-scaling also allows, if you choose a stack with a very fast boot-time like NodeJS, Python or Go, for scaling down to zero. This requires some additional effort to make sure that the performance of the app allow for instant “warm up” of new lambdas. But once that is done, it is possible to turn the whole infrastructure off by default and just turn it on, on demand, while a user is interacting with the app.

### **Main trade-offs?**

#### Trade-off #1: Getting married to a cloud provider

#### Trade-off #2: leveraging well requires a very different way to architecture the code. 

Back to NoSQL, stateless backend, rich frontend

#### Trade-off #3: The technology is still quite new