---
layout: archive
permalink: /lecture/
title: "Posts by Year"
author_profile: true
---

{% include base_path %}
{% capture written_year %}'None'{% endcapture %}
{% for post in site.lecturenotes %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
    <h2 id="{{ year | slugify }}" class="archive__subtitle">{{ year }}</h2>
    {% capture written_year %}{{ year }}{% endcapture %}
  {% include archive-single.html %}
{% endfor %}