---
layout: post
title: Hibernate Note
description: "This note is about the problems that I met while using Hibernate."
modified: 2013-04-01
tags: [Hibernate, Database]
comments: false
image:
  feature: 2010-06-01-hibernate.png
---

This note is about the problems that I met while using Docker.

# 1. Generated Value

{% highlight html %}
@Id
@GeneratedValue(generator = "uuid")
@GenericGenerator(name = "uuid", strategy = "uuid2")
{% endhighlight %}
