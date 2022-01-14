---
layout: default
description: Single cell analysis in epigenetics research - a practical course for students of the LMU Munich
---

## Course schedule
<a class="btn btn-primary" role="button" data-toggle="collapse" href="#schedule" aria-expanded="false" aria-controls="python_basics">
  Course schedule
</a>
<a class="btn btn-primary" role="button" href="https://github.com/IES-HelmholtzZentrumMunchen/single-cell-analysis-course-2022/raw/master/pdf/schedule.pdf">
  Download schedule as PDF
</a>

<div class="collapse" id="schedule">
  <div class="embed-responsive embed-responsive-4by3">
    <iframe class="embed-responsive-item" title="Schedule" src="{{'/html/schedule.html' | prepend: site.url }}">
  </div>
</div>


{% assign sorted = site.collections | sort: 'label' %}

{% for collection in sorted %}
{% unless collection.label == "posts" %}
## {{ collection.label | replace: "_"," " | capitalize  }}
{: .bg-section }

{{ collection.docs}}
{% endunless %}
{% endfor %}
