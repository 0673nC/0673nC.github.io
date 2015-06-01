---
layout: layout
title: 0673nC's Blog
---
#個人的メモ用のブログ.

{% for post in site.posts %}
<div class="panel panel-primary">
  <div class="panel-heading">
    <h3 class="panel-title">
      <a href="{{ post.url }}">{{ post.title }}</a>
    </h3>
  </div>
  <div class="panel-body">
  <span class="lead">{{ post.date | date_to_long_string }} : </span>
  {% for tag in post.tags %}
    <a href="#" class="btn btn-success">{{ tag }}</a>
  {% endfor %}
  </div>
</div>
{% endfor %}
