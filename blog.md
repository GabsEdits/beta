---
title: Blog
layout: comingsoon
---

{% assign posts = site.posts | sort: "date" | sort: "updated" | reverse %}

{% for post in posts %}
    {% if post.is_translation == false %}
        {% include posts-listing.html post=post %}
    {% endif %}
{% endfor %}