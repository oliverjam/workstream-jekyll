---
layout: default
---

{% assign sections = site.sections | sort:"position" %}
{% for section in sections %}
  {% if section.include != null %}
    {% include {{ section.include }} %}
  {% else %}
    {% include sections/generic.html %}
  {% endif %}
{% endfor %}
