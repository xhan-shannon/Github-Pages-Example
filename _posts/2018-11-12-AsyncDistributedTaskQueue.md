---
layout: post
title: asynchronous task queues
description: asynchronous task queues 
category: blog
---

Task
There would be producers and consumers for two or more independed processes. And the message or task description can be saved into files. The problem with text files is that they are not made to handle real application problems such as network and concurrent access. SQL databases, on the other hand, are capable of running in a network and dealing with concurrent access. The problem with them is that they are too slow. NoSQL databases, by contrast, are quite fast, but many times they lack reliability. So, when building queues, we should use fast, reliable, concurrency enabled tools such as RabbitMQ, Redis and SQS.

Work flow:
Producer --> Broker  --> Worker <--> Result Backend


Best practices:
1. Avoid passing complex objects as parameters
2. 

https://codepath.org

[Shannonh]:    https://github.com/xhan-shannon "xhan-shannon"

