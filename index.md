---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

<!-- show all the posts -->

<ul>
  {% for post in site.posts %}
    <li>
       <a href="{{ post.url }}">{{ post.title }}</a>
       <!-- how to overwrite ro -->
       <span class="post-words">
       ({{ post.content | number_of_words }} words, {{ post.date | date: "%m/%d/%y"}} )
       </span>
    </li>
  {% endfor %}
</ul>
