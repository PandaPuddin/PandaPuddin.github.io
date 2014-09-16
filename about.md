---
layout: page
permalink: /about/index.html
title: PandaPuddin
tags: [Panda, Puddin, PandaPuddin]
imagefeature: fourseasons.jpg
chart: true
---

{% assign total_words = 0 %}
{% assign total_readtime = 0 %}
{% assign featuredcount = 0 %}
{% assign statuscount = 0 %}

{% for post in site.posts %}
    {% assign post_words = post.content | strip_html | number_of_words %}
    {% assign readtime = post_words | append: '.0' | divided_by:200 %}
    {% assign total_words = total_words | plus: post_words %}
    {% assign total_readtime = total_readtime | plus: readtime %}
    {% if post.featured %}
    {% assign featuredcount = featuredcount | plus: 1 %}
    {% endif %}
{% endfor %}


Hi.
You seem to have stumbled across my blog! 
I'm a pretty simple person. I love cooking and baking, photography, mysteries of all kinds (namely, Sherlock), and pandas. You'll find all sorts of things here. 
Hopefully I'll have some more content soon!
