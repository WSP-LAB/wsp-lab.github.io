---
layout: default
---

## Teaching
<ul>
{% for class_info in site.teaching %}
<li><code>{{ class_info.code }}</code> {% if class_info.link %}<a href="{{ class_info.link }}">{{ class_info.name }}</a>{% else %}{{ class_info.name }}{% endif %} {% if class_info.semastors %}({% for semastor in class_info.semastors %}{% if semastor.link %}<a href="{{ semastor.link }}">{{ semastor.name }}</a>{% else %}{{ semastor.name }}{% endif %}{% if forloop.last == false %}, {% endif %}{% endfor %}){% endif %}</li>{% endfor %}
</ul>
