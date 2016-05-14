---
layout: page
title: Ausstellung
permalink: /de/exhibition
name: exhibition
lang: de
---


{% for list in site.data.games %}
<div class="row blog-list">
	{% if list[1].digital != "yes" %}
  <div class="third">
  	<a class="image" {% if list[1].digital != "openscreen" %}href="{{ list[1].url }}"{%endif%}><img style="width: 100%; object-fit: cover; height: 12rem; margin:0;" src="{{ site.baseurl }}/assets/img/{{ list[1].img }}"></a>
  </div>
  	{%endif%}
  <div class="two-third" style="padding-bottom:2rem">
  	<b>{{ list[1].title }}</b><br>{% if list[1].by %}{{list[1].by}}{%endif%}{% if list[1].bylong %} {{ list[1].bylong}}{%endif%}<br><br>{% if list[1].digital != "openscreen" %}<a href="{{ list[1].url }}">{{ list[1].url }}</a>{%endif%}{% if list[1].digital == "yes" %}<i>Teil der digitalen Kuration.</i>{%endif%}
  </div>
  {% if list[1].digital == "yes" %}
  <div class="third">
  	<a class="image" {% if list[1].digital != "openscreen" %}href="{{ list[1].url }}"{%endif%}><img style="width: 100%; object-fit: cover; height: 12rem; margin:0;" src="{{ site.baseurl }}/assets/img/{{ list[1].img }}"></a>
  </div>
  	{%endif%}
</div>
{% endfor %}