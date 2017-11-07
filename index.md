---
title: Welcome!
---

Hello the internet! This is a my little space on the interweb.
You can find posts about technology, programming and hacking on here.

Here is a nice image for your viewing pleasure:

![Flashy gif animation]({{ site.url }}/assets/images/welcome.gif)



Read all the blog posts:
========================


<div>
  {% assign postsByYearMonth = site.posts | group_by_exp:"post", "post.date | date: '%Y %b'"  %}
  {% for yearMonth in postsByYearMonth %}
    <h3>{{ yearMonth.name }}</h3>
      <ul>
        {% assign sorted = (yearMonth.items | sort: 'date') %}
        {% for post in sorted %}
          <li><a href="{{ post.url }}">{{ post.title }}</a></li>
        {% endfor %}
      </ul>
  {% endfor %}
</div>


Sorted by tags:
---------------

<div>
  <ul>
  {% for tag in site.tags %}
    <li style="font-size: {{ tag | last | size | times: 100 | divided_by: site.tags.size | plus: 70 }}%">
        <a href="/{{ tag | first | slugize }}/">
            {{ tag | first }} ({{ tag | last | size }})
        </a>
    </li>
  {% endfor %}
  </ul>
<div>
