---
layout: page
title: Blog posts
permalink: /blog/
---
<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

      <h2>
        <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        <div class="categories flex-row">
          {% for cat in post.categories %}
            <span class="basic-flex post-meta category">{{ cat }}</span>
          {% endfor %}
        </div>
      </h2>
    </li>
  {% endfor %}
</ul>

<p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>
