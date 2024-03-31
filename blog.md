---
title: Bits
layout: post
---

<!-- show all the posts -->
<!-- show the same context in index.md -->

<ul>
  {% for post in site.posts %}
    <li style="list-style: none;">
    {{ post.date | date: "%m/%d/%y"}} -
       <a href="{{ post.url }}">{{ post.title }}</a>
       <!-- how to overwrite ro -->
       <span class="post-words">
       ({{ post.content | number_of_words }} words)
       </span>
    </li>
  {% endfor %}
</ul>
