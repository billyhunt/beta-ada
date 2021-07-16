---
permalink: /topics/
title: How the ADA Works
sidenav: false
show_card: false
lead: |-
  Information for businesses, state and local governments, and people with disabilities.
---

{% assign pages = site.pages | where_exp:"item","item.permalink contains '/topics/' and item.name != 'index.md'" %}

{% assign cards = pages | concat: site.data.cards %}

<div class="grid-row grid-gap">
  <ul class="usa-card-group">
    {% for card in cards %}
      {% include card.html card=card heading_level=2 %}
    {% endfor %}
  </ul>
</div>