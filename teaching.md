---
layout: default
---

## Teaching
<ul>
{% for class_info in site.teaching %}
<li><code>{{ class_info.code }}</code> {% if class_info.link %}<a href="{{ class_info.link }}">{{ class_info.name }}</a>{% else %}{{ class_info.name }}{% endif %} {% if class_info.semesters %}({% for semester in class_info.semesters %}{% if semester.link %}<a href="{{ semester.link }}">{{ semester.name }}</a>{% else %}{{ semester.name }}{% endif %}{% if forloop.last == false %}, {% endif %}{% endfor %}){% endif %}</li>{% endfor %}
</ul>
