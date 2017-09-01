
Read all the blog posts:
------------------------

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

Hello the internet! This is a my little space on the interweb.
You can find posts about technology, programming and hacking on here.



Here is a nice image for your viewing pleasure:

![Flashy gif animation](https://media.giphy.com/media/zhbrTTpmSCYog/giphy.gif)
