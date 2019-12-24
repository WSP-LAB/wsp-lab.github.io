---
layout: default
---
## Publication
{% for pub_group in site.publication %}<h3>{{ pub_group.year }}</h3>
<ul>{% for item in pub_group.list %}
<li>
{{ item.authors }}. <a href="{{ item.link }}">{{ item.title }}</a>{% if item.published == false %}(to appear){% endif %}
<ul>
<li>{{ item.booktitle }}</li>{% for comment in item.comments %}<li>{{ comment }}</li>{% endfor %}
</ul>
</li>
{% endfor %}
</ul>
{% if forloop.last == false %}<hr>{% endif %}
{% endfor %}
