---
layout: default
---
## Publications
<ul>
 <li><font style="color:#0b5394;"><strong>[*Security] Security Top Conferences:</strong></font> S&P (Oakland), ACM CCS, USENIX Security, NDSS </li>
 <li><font style="color:#0b5394;"><strong>[*CS] Published CS Top Conferences:</strong></font> WWW, PLDI, OOPSLA </li>
</ul> 
{% for pub_group in site.publications %}
<h3>{{ pub_group.year }}</h3>
<ul>
{% for item in pub_group.list %}
  <li>
    <strong>
      {% if item.toptier_security == true %}
      <font style="color:#0b5394;">[*Security] </font>
      {% elsif item.toptier_cs == true %}
      <font style="color:#0b5394;">[*CS] </font> 
      {% endif %}
      {{item.title}}{% if item.published == false %} (to appear){% endif %}
    </strong>
    <ul>
      <li>{{ item.authors }}.</li>
      <li><em>{{ item.booktitle }}</em></li>
      {% for comment in item.comments %}
      <li>{{ comment }}</li>
      {% endfor %}
      {% if item.published == true %}
      <li>
        [<a href="{{ item.link }}">paper</a>]
        {% if item.code %}
        [<a href="{{ item.code }}">code</a>]
        {% endif %}
        {% if item.media %}
        [<a href="{{ item.media }}">media</a>]
        {% endif %}
      </li>
      {% endif %}
    </ul>
  </li>
  <br>
{% endfor %}
</ul>
{% if forloop.last == false %}<hr>{% endif %}
{% endfor %}
