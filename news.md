---
title: News
layout: about
classes: about news
meta-description: News about Ergo.chat.
logo: ergo-logo-dark.svg
---
This page contains news about the Ergo IRC server, the Ergo IRC network, new releases, and plans for the future.

We also have an RSS feed here, which you can use to keep updated: [feed.xml](https://ergo.chat/feed.xml)

-----

{% for post in site.posts %}
{% assign author = site.data.authors[post.author] %}

<h2>{{ post.title }}</h2>

<p class="postinfo">{% if author.name %}[{{ author.name }}]({{ author.web }}) - {% endif %}{{ post.date | date_to_string }} - <a href="{{ site.liveurl }}{{ post.url }}">Link</a></p>

{{ post.content }}

{% if forloop.last %}{% else %}<hr>{% endif %}
{% endfor %}
