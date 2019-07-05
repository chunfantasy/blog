---
layout: post
title: Hibernate Note
description: "This note is about the problems that I met while using Hibernate."
modified: 2013-04-01
tags: [Framework]
comments: true
image:
  feature: 2010-06-01-hibernate.png
---

This note is about the problems that I met while using Hibernate.

<div id="ckepop">
<span class="jiathis_txt">分享到：</span>
<a class="jiathis_button_weixin">微信</a>
<a class="jiathis_button_tsina">微博</a>
<a href="http://www.jiathis.com/share?uid=2074997"  class="jiathis jiathis_txt jiathis_separator jtico jtico_jiathis" target="_blank">更多</a></div>
<script type="text/javascript" src="http://v3.jiathis.com/code/jia.js?uid=2074997" charset="utf-8"></script>

# Generated Value

{% highlight java %}
@Id
@GeneratedValue(generator = "uuid")
@GenericGenerator(name = "uuid", strategy = "uuid2")
{% endhighlight %}

# Mapping

{% highlight java %}
// One to one
@OneToOne(cascade = {CascadeType.PERSIST, CascadeType.REFRESH})
@JoinColumn(name = "memberId")
{% endhighlight %}

* CascadeType.PERSIST : means that save() or persist() operations cascade to related entities.
* CascadeType.MERGE : means that related entities are merged into managed state when the owning entity is merged.
* CascadeType.REFRESH : does the same thing for the refresh() operation.
* CascadeType.REMOVE : removes all related entities association with this setting when the owning entity is deleted.
* CascadeType.DETACH : detaches all related entities if a “manual detach” occurs.
* CascadeType.ALL : is shorthand for all of the above cascade operations.