---
layout: page
title: Welcome!
tagline: The index page
---
<div id="home">

  <div id="featured">
    <h3>Latest</h3>
    {% for post in site.posts offset: 0 limit: site.theme.homepage_featured %}
    <article>
      <h2>{{ post.date | date_to_string }}</h2>
      <h1><a href="{{ post.url }}">{{ post.title }}</a></h1>
      <p class="baseline">{{ post.baseline }}</p>
      <p>{{ post.content | strip_html | truncatewords: site.theme.featured_wordcount }}</p>
      <p><a href="{{ post.url }}" class="more">Read more »</a></p>
    </article>
    {% endfor %}
  </div>

  <div id="posts">
    <h3>Previous posts</h3>

    <dl>
      {% for post in site.posts offset: site.theme.homepage_featured limit: site.theme.homepage_posts %}
        <dt>{{ post.date | date_to_string }}</dt>
        <dd><a href="{{ post.url }}">{{ post.title }}</a></dd>
      {% endfor %}
    </dl>
    <p><a href="/archive.html" class="more">View all posts »</a></p>
  </div>

</div>
