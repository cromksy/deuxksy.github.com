---
layout: page
title: Categories
permalink: /categoreis/
---
<div class="archive">
{% for category in site.categories %}
    <div class="archive-group">
      {% capture category_name %}{{ category | first }}{% endcapture %}
      <h3 class="category-head">{{ category_name }}</h3>
      {% for post in site.categories[category_name] %}
      <article class="archive-item">
        <h4><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h4>
      </article>
      {% endfor %}
    </div>
{% endfor %}
</div>
