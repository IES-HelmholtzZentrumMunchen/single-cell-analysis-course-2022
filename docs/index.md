---
layout: default
description: Single cell analysis in epigenetics research - a practical course for students of the LMU Munich
---

## Schedule
{% assign other = site.other %}
{% assign homework = site.homework | concat: other %}
{% assign exercise = site.exercise | concat: other %}
{% assign lectures = site.lectures | concat: exercise  %}
{% assign lectures_sorted = lectures | sort: "date" %}

{% assign prevdate = "0" %}
<table class="table table-bordered">
  {% for lecture in lectures_sorted %}

  {% assign thedate = lecture.date | date: "%d" %}
  {% assign handle = lecture.collection %}

    {% if lecture.collection == "lectures" %}
      {% assign tblstyle = "background-color: #ffccaa;" %}
    {% elsif lecture.collection == "exercises" %}
      {% assign tblstyle = "background-color: #99ddff;" %}
    {% elsif lecture.collection == "other" %}
      {% assign tblstyle = "background-color: #eeeebb;" %}
    {% else %}
      {% assign tblstyle = "background-color: #ffffff;" %}
    {% endif %}


    {% if thedate != prevdate %}
      <tr>
        <td colspan="2" style="font-size: 2rem; font-weight: bold;">
        {{ lecture.date | date: "%A, %d %B" }}
        </td>
      </tr>
      {% assign prevdate = thedate %}
    {% endif %}

      <tr>
        <td style="{{ tblstyle}}">
            {% if lecture.title contains "Assignment" %}due: {% endif%} {{ lecture.date | date: "%H:%M" }} {% if lecture.end %} - {{ lecture.end | date: "%H:%M" }} {% endif %}
        </td>
        <td style="{{ tblstyle}}">
          <a href="#{{ lecture.title | downcase | replace: "'","" | replace: ",", "" | replace: " ", "-" | replace: ")", "" | replace: "(","" }}">{{ lecture.title }}</a>
        </td>
      </tr>

  {% endfor %}
</table>


{% assign sorted = site.collections | sort: 'label' | reverse %}

{% for collection in sorted %}
{% unless collection.label == "other" %}
## {{collection.label | replace: "_"," " | capitalize  }}
{: .bg-section }

{{ collection.docs}}
{% endunless %}
{% endfor %}
