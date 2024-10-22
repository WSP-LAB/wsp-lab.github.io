---
layout: default
---
## Publications
<ul>
 <li><font style="color:#0b5394;"><strong>[*Top-tier] Security Top Conferences:</strong></font> S&P (Oakland), ACM CCS, USENIX Security, and NDSS </li>
 <li><font style="color:#b300b3;"><strong>[*Top-tier] Published CS Top Conferences:</strong></font> WWW, NeurIPS, ICML, PLDI, OOPSLA, and MobiSys </li>
</ul> 
{% for pub_group in site.publications %}
<h3>{{ pub_group.year }}</h3>
<ul>
{% for item in pub_group.list %}
  <li>
    <strong>
      {% if item.toptier_security == true %}
      <font style="color:#0b5394;">[*Top-tier] </font>
      {% elsif item.toptier_cs == true %}
      <font style="color:#b300b3;">[*Top-tier] </font> 
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
