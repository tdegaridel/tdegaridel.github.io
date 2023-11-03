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

{% bibliography -f {{ site.scholar.bibliography }} --group_by type %}

</div>
