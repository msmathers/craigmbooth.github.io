---
layout: page
title: All Posts
excerpt: "An archive of blog posts sorted by date."
search_omit: true
image:
  feature: headers/blog_header.jpg
---

This page contains a list of all of the posts on this blog.  I generally write about programming and data related subjects, but every now and again something else catches my eye.  If you know what you're looking for, you could browse all [posts by tag](/tags).

<ul class="post-list">
{% for post in site.posts limit:100 %}
  <li>
    <article>
      <a href="{{ post.url }}">
        {{ post.title }}
        <span class="entry-date">
          <time datetime="{{ post.date | date_to_xmlschema }}">
            {{ post.date | date: "%B %d, %Y" }}
          </time>
        </span>
        {% if post.excerpt %}
          <span class="excerpt">
            {{ post.excerpt }}
          </span>{% endif %}
      </a>
    </article>
  </li>
{% endfor %}
