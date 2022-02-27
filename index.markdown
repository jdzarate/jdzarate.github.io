---
layout: default
title: jdzarate.com
---
<div id="home" style="">
  <ul class="posts">
    {% for post in site.categories.blog limit:6%}

      {% if forloop.first %}
      <div class="post-container firstpost">
        <span class="post-date">{{ post.date | date_to_string }}</span>
        <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
        <div class="post">
        {{ post.content }}
        </div>
      </div>
      <hr>
      {% else%}
      <li>
         <span>{{ post.date | date_to_string }}</span>&nbsp;&nbsp;<a href="{{ post.url }}" class="post-name" style="">{{ post.title }}</a>
         
      </li>
      {% endif %}
      
    {% endfor %}
  </ul>

  <p><a href="/archive">Ver más publicaciones</a></p>
</div>