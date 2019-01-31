---
layout: subpage
title: Legalist Ethics
image: css/yang.png
subpage: true
coursepage: false
---
<link rel="stylesheet" href="/ethical-computing-institute/css/legalist.css">

## “If in a c untry there are the following ten evils: rites, music, odes, history, virtue, moral culture, filial piety, brotherly duty, integrity and sophistry, the ruler cannot make the people fight and dismemberment is inevitable; and this brings extinction in its train.”
### - Shang Yang, *The Book of Lord Shang*

## Blog Posts

{% for post in site.categories.legalism %}
  <a href="{{ site.baseurl | append: post.url }}">{{ post.title }} ( {{post.date }} )</a><br>
{% endfor %}
