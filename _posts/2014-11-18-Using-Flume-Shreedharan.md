---
layout: post
title: Using Flume, By Hari Shreedharan
---

![](https://cloud.githubusercontent.com/assets/790974/5087789/9120195e-6f2c-11e4-9b4f-acf65993c342.gif)

See it on [Amazon][azn].

I've just read *Using Flume* by [Hari Shreedharan][author]. I'm spending quite a lot of time with Hadoop 
and ElasticSearch lately. While I'm in dev, everything is "easy". However, thinking about my system running
for about 30M users , and things get more complicated :).

I've picked-up this book because Flume came quite often in my researchs, and the author has created Flume ;)

## What's inside?

The first chapter recalls what is Apache Hadoop and HBase. If you know Hadoop, it's not required, but I've learn few things. Chapter 2 gives you the big picture about Flume, and few hints about the history of the project.

Then, the main part of the book - chapters 3, 4, 5 and 6 - covers in details each main Flume components. I'm not a java guy, 
but I appreciate this book covers how to extend Flume.

The chapter 7 covers how to send data from your app to Flume. I'm quite disappointed it's only covers how to send data from Java apps. There even no mention to existing clients, like [.net flume NG client][flumengnet].

The chapter 8 covers how to plan and deploy Flume. I didn't deploy Flume to production, but it seems that the plan part is well covered.

## Bottom line

If you want to manage a stream of data to go from one point to a big data system (Hadoop, ElasticSearch, ...),
Flume may be your best choice. If Flume is your choice, then, this book is your best first step in learning Flume.


> *Disclosure*: O'Reilly send me a free copy of this ebook in exchange for this review.

[azn]: http://www.amazon.com/gp/product/1449368301/ref=as_li_tl?ie=UTF8&camp=1789&creative=390957&creativeASIN=1449368301&linkCode=as2&tag=chriscorn02-20&linkId=T3RGLSECZ2DZVMUL
[author]: https://twitter.com/harisr1234
[flumengnet]: https://github.com/marksl/DotNetFlumeNG.Clients
