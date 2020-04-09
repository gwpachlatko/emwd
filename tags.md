---
layout: page
title: Tags
permalink: /tags/
lang: de
---

{% comment %}
=======================
extract all tags from posts and sort them
=======================
{% endcomment %}
{% assign rawtags = "" %}
{% for post in site.posts %}
	{% assign ttags = post.tags | join:'|' | append:'|' %}
	{% assign rawtags = rawtags | append:ttags %}
{% endfor %}
{% assign rawtags = rawtags | split:'|' | sort %}

{% comment %}
=======================
remove dulpicated and invalid tags
=======================
{% endcomment %}
{% assign tags = "" %}
{% for tag in rawtags %}
	{% if tag != "" %}
		{% if tags == "" %}
			{% assign tags = tag | split:'|' %}
		{% endif %}
		{% unless tags contains tag %}
			{% assign tags = tags | join:'|' | append:'|' | append:tag | split:'|' %}
		{% endunless %}
	{% endif %}
{% endfor %}

{% comment %}
=======================
list all posts sharing a certain tag
=======================
{% endcomment %}

{% for tag in tags %}
<dl>
	<dt id="{{ tag | slugify }}">{{ tag }}</dt>

	 {% for post in site.posts %}
		 {% if post.tags contains tag %}
		 <dd>
		 <a href="{{site.baseurl}}{{ post.url }}">
		 {{ post.title }}</a> <small>am {% include translated_date.html date=post.date format="%-d. %b %Y" %}</small>
		</dd>
		 {% endif %}
	 {% endfor %}
	</dl>
{% endfor %}
