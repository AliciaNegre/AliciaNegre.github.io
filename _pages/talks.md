---
title: "Talks"
layout: gridlay
sitemap: false
permalink: /talks/
---

## Talks

<div class="section-card" id="pubList">
<h3>Invited Talks</h3>

{% bibliography --query @incollection[keywords ^= invited] %}

<h3>Regular Talks</h3>

{% bibliography --query @incollection[keywords != invited && keywords != poster] %}

<h3>Posters</h3>

{% bibliography --query @incollection[keywords ^= poster] %}
</div>
