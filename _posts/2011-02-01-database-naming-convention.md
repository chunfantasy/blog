---
layout: post
title: Database Naming Convention
description: "This note is about the convention when design a database."
modified: 2011-02-01
tags: [Database]
comments: true
---

This note is about the problems that I met while using Docker.

# 1. Install

Just use apt-get install, easy, fast and enough to use.

{% highlight html %}
$ sudo apt-get install mysql-server
{% endhighlight %}

# 2. Create User

Read the doc from official site.

{% highlight html %}
mysql> CREATE USER 'monty'@'%' IDENTIFIED BY 'some_pass';
{% endhighlight %}

# 3. Grant

Read the doc from official site.

{% highlight html %}
mysql> GRANT ALL ON db1.* TO 'jeffrey'@'localhost';
{% endhighlight %}

# 4. Encoding

Show the encoding type of current database.

{% highlight html %}
mysql> show variables like "character_set_database";
mysql> show variables like "collation_database";
{% endhighlight %}