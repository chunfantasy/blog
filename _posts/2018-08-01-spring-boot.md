---
layout: post
title: Spring Boot
description: "This note is about the configuration of testing environment with Spring Boot."
modified: 2018-08-01
tags: [Framework]
comments: true
---

This note is about the configuration of testing environment with Spring Boot.

# Spring Component

## Start application

{% highlight kotlin %}
@SpringBootApplication
@ComponentScan("chun.api")
class ApiApplication {

}

fun main(args: Array<String>) {
    runApplication<ApiApplication>(*args)
}
{% endhighlight %}
