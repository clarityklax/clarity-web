---
title: Clarity of thought
---

<nav class="site-nav">
  <a href="/blog">Blog</a>
  <a href="/legal">Legal</a>
</nav>

<div class="intro" markdown="1">

Hi, I'm [Ivan Klaric](https://www.linkedin.com/in/iklaric/) -- a software engineer (these days mostly a manager) who occasionally [writes](/blog). I like to think I bring clarity to engineering teams, hence the domain (and the name of the legal entity behind it).

</div>

<p class="section-label">Recent writing</p>

<ul class="recent-posts">
{% assign recent_posts = site.posts | slice: 0, 5 %}
{% for post in recent_posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="post-date">{{ post.date | date: "%b %Y" }}</span>
  </li>
{% endfor %}
</ul>

<a href="/blog" class="view-all">All posts &rarr;</a>
