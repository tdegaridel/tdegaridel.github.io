---
layout: page
permalink: /publications/
title: publications
description: Publications by categories in reversed chronological order. Submitted manuscripts indicated as working papers - the date corresponds to the initial submission.
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

// {% bibliography -f {{ site.scholar.bibliography }} --group_by type %}

//<!-- filepath: /Users/garidel/Documents/GitHub/tdegaridel.github.io/_pages/publications.md -->
//<div class="publications">

{% assign pubs = site.bibliography | sort: "year" | reverse %}
{% assign types = pubs | map: "type" | uniq %}

{% for type in types %}
  <h2>{{ type | capitalize }}</h2>
  <ol>
    {% assign pubs_of_type = pubs | where: "type", type %}
    {% for pub in pubs_of_type %}
      <li>
        {{ pub }}
      </li>
    {% endfor %}
  </ol>
{% endfor %}


</div>
