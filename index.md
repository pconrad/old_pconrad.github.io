---
layout: default
title: Articles by Phill Conrad
---

# {{page.title}}

<div id="info" data-role="collapsible" data-collapsed="false">
<h2>Page Information</h2>
This site is a collection of articles by Phill Conrad on various
topics.
</div>

<div data-role="collapsible" data-collapsed="false">
<h2 id="labs">Topics</h2>
 <ul>
 {% for item in site.topics %}
   <li><a href="{{item.url}}">{{item.topic}}&mdash;{{item.desc}}</a></li>
 {% endfor %}
 </ul>
</div>



