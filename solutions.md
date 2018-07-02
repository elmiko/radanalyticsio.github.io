---
layout: markdown
title: Solutions
menu_entry: Solutions
---

# Solutions

These solutions have been designed to showcase technologies and design
patterns that can be used to begin creating intelligent applications on
OpenShift. They are fully integrated application pipelines which illustrate
how an idea, methodology or technology can be developed and deployed on
OpenShift in a manner that users can experience the underlying analytics in
a more convenient manner.

All of these solutions contain instructions for installation and usage as
well as open source code artifacts that you are welcome to clone and use
in your own projects and presentations. They also contain
videos and slide decks that can be helpful when presenting or demonstrating
them to your peers and colleagues.

<div class="row row-cards-pf">

{% assign sorted_applications = site.applications | sort: 'weight' %}
{% for item in sorted_applications %}
<div class="col-xs-12 col-sm-12 col-md-12 col-lg-12">
<a href="/applications/{{ item.link }}" class="card">
<div class="card-pf card-pf-view card-pf-view-select card-pf-accented">
<div class="card-pf-body" style="">

<span class="theme pull-right">{{ item.theme }}</span>

<h2>
{{ item.title }}
{% for label in item.labels %}
<span class="badge">{{ label }}</span>
{% endfor %}
</h2>

<p>
{{ item.description }}
</p>

{% if item.project_links %}
<h4>Project Links</h4>

<ul>
{% for link in item.project_links %}
<li><a href="{{ link }}" target="blank">{{ link }}</a></li>
{% endfor %}
</ul>
{% endif %}

</div>
</div>
</a>
</div>
{% endfor %}

</div>
