---
layout: default
title: young only
description: This blog serves as documentation for Neil's progress in webmastering as well as to share some thoughts, insights and daily happenings.
---

<p style="text-align:center">Commentary through creative means
<br/>
<br/>---</p>
<section class="archive-post-list" style="align:center">
   {% for post in site.posts %}
       {% assign currentDate = post.date | date: "%Y" %}
       {% if currentDate != myDate %}
           {% unless forloop.first %}</ul>{% endunless %}
           <ul>
           {% assign myDate = currentDate %}
       {% endif %}
       <li>
       <span class="title" style="text-transform:lowercase"><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></span>
       <span class="date">{{ post.date | date: "%B %-d, %Y" }}</span>
       </li>
       {% if forloop.last %}</ul>{% endif %}
   {% endfor %}

</section>
