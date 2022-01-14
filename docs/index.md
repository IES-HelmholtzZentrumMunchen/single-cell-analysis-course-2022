---
layout: default
description: Single cell analysis in epigenetics research - a practical course for students of the LMU Munich
---


{% assign sorted = site.collections | sort: 'label' %}

{% for collection in sorted %}
{% unless collection.label == "posts" %}
## {{ collection.label  | replace: "_"," " | slice: 3, collection.label.size | capitalize  }}
{: .bg-section }

{{ collection.docs}}
{% endunless %}
{% endfor %}
