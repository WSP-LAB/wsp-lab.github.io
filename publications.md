---
layout: default
---
## Publications
{% for pub_group in site.publications %}
<h3>{{ pub_group.year }}</h3>
<ul>
{% for item in pub_group.list %}
  <li>
    {{item.title}}{% if item.published == false %} (to appear){% endif %}
    <ul>
      <li>{{ item.authors }}.</li>
      <li>{{ item.booktitle }}</li>
      {% if item.published == true %}
      <li>[<a href="{{ item.link }}">paper</a>]</li>
      {% endif %}
      {% for comment in item.comments %}
        <li>{{ comment }}</li>
      {% endfor %}
    </ul>
  </li>
  <br>
{% endfor %}
</ul>
{% if forloop.last == false %}<hr>{% endif %}
{% endfor %}
