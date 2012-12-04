---
layout: page
title: Welcome!
tagline: The index page
---
<div id="home">

  <div id="posts">
    {% for post in site.posts offset: 0 limit: 6 %}
    <article>
      <h2>{{ post.date | date_to_string }}</h2>
      <h1><a href="{{ post.url }}">{{ post.title }}</a></h1>
      <p class="baseline">{{ post.baseline }}</p>
      <p>{{ post.content }}</p>
      <p><a href="{{ post.url }}" class="more">Read more »</a></p>
    </article>
    {% endfor %}
  </div>

  <p><a href="/archive.html" class="more">View all posts »</a></p>

</div>
