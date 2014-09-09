---
layout: post
title: High-Performance Windows Phone Apps
---

![_config.yml]({{ site.baseurl }}/images/2014-9-1-High-performance-windows-phone-apps.jpg)

See it on [Amazon][azn].

I've just read *High-Performance Windows Store Apps* by [Brian Rasmussen][author].
It's what not on my reading list, but as I've undergone a "performance sprint",
I thought it was a good timing.

## What's inside ?

The first chapter explains what is performance, and what we need to focus on when
we start working on this subject. The core of this book is **Windows Performance analyzer** tool. Lots of pages are
dedicated to see how you can use this tool to trace performance data, investigate
performance issues, and so on. It's, by far, the best documentation on this tool
I found. So, the chapter 1 also introduces this tool.

The chapter 2 explains the Windows Store apps platform architecture (how an app is booted,
how your C# code integrates with the WinRT runtime, etc...). It also explains where
performance issues can hit you: UI Thread, Binding, images, WinRT interop calls,
animations, etc...

The chapter 3 - "Designing for performance" is a broader chapter, and can be read by
a project manager, product owner or even a designer. Basically, it explains that you
can always try to optimize a specific function or limiting overdraw on a particular
control. But if you take performance seriously, you need to take performance into
account at the feature design stage. It also explains "general tricks" (http caching,
partitioning, UI virtualization) or Windows Store specific tricks (ContentPrefetcher)
to help you optimize the performance of your app quite quickly.

Chapter 4 dive into the tools available to measure your app performance. It talks
about Event Tracing for Windows, WinRT instrumentation and EventSource-based instrumentation.
It's a good introduction to these subjects, but not a deep dive.

I was quite disappointed by the chapter 5 - Performance testing. I was aiming at
real-world solutions to automate performance testing. However, this book covers only
the basics of creating coded UI testing, and hand-made code to collect performance
date from event trace. It seems that there is no ready-to-use solutions. You'll need
to build all the infrastructure : launching the test, collecting the data, saving
the results and compare it over time.

The chapter 6 presents three "performance issues investigations":

- slow startup: caused by too much work done on a value converter,
- slow page navigation: caused by messing up with async/await, lots of I/Os and all
of this done in the constructor.  ,
- sluggish panning performance: caused by too much overdraw, and full-size images
used in thumbnails.

The chapter 7 is basically a list of additional resources on performance (videos, online resources, ...).

## Bottom line

I would not recommend this book if you already have an experience in performance on
the XAML platform. I was hoping for more practical solutions (mainly in the performance
  testing area), and insider view in the XAML platform. However, if you want to discover the basics of XAML app performance
(and more specific - Windows Store apps performance), this book is a good way to be started.


[azn]: http://www.amazon.com/gp/product/0735682631?ie=UTF8&camp=213733&creative=393185&creativeASIN=0735682631&linkCode=shr&tag=chriscorn02-20&linkId=MN67DC3ZWOQR2PSH&qid=1409586892&sr=8-1-spell&keywords=High+performance+windows+stpre+apps
[author]: https://twitter.com/kodehoved
