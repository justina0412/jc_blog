layout: post
title: "Blog 9"
---

AWS Application Load Balancer
------------------------------

The AWS load balancer is the single point of contact for clients to availability zones (AZs). It distributes incoming application traffic across multiple targets (ec2 instance).


The purpose of a load balancer is to increase the availability of an application.
It contains listeners which check for connection requests from clients.

The load balancer also Monitors the health of the targets (ec2). If targets are unhealthy, the load balancer with stop routing traffic.

![Load Balncer Diagrem](

https://s3-us-west-2.amazonaws.com/us-west-2-aws-training/awsu-spl/spl-68/images/diagram.png

  )
