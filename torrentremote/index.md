---
title: Torrent Remote
description: A few words about our Torrent Remote app.
resource: true
categories: [torrent-remote]
---

{% for cat in site.category-list %}
<!-- ### {{ cat }} -->
<ul>
  {% for page in site.pages %}
    {% if page.resource == true %}
      {% for pc in page.categories %}
        {% if pc == cat %}
          <li><a href="{{ page.url }}">{{ page.title }}</a></li>
        {% endif %}   <!-- cat-match-p -->
      {% endfor %}  <!-- page-category -->
    {% endif %}   <!-- resource-p -->
  {% endfor %}  <!-- page -->
</ul>
{% endfor %}  <!-- cat -->

## Welcome to the documentation for the Torrent Remote Windows Store app

We've added some helpful links below to guide you on your way!

- [Getting started](getting-started/index.html)
- [Turning on the Web UI in uTorrent](getting-started/turning-on-web-ui.html)
- [Setting up for access on a local network](getting-started/setting-up-for-access-on-a-local-network.html)

Over time you will see new information on this portal page, so stay tuned!

## Our mentions

We've been mentioned on Softpedia! Check it out!

  - [Download uTorrent Client for Windows 8 - Softpedia](http://news.softpedia.com/news/Download-uTorrent-Client-for-Windows-8-315970.shtml)
- [uTorrent Client for Windows 8 Updated and Released for Download - Softpedia](http://news.softpedia.com/news/uTorrent-Client-for-Windows-8-Updated-and-Released-for-Download-317351.shtml)
