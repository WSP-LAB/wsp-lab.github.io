---
layout: default
---

## Research Area
Web Security & Privacy (WSP) Lab  conducts research on various topics regarding web 
security and privacy. We envision making Internet services more secure and private
by contemplating novel ideas and implementing them in real-world services.
Our research topics can be categorized into four research directions:

- R1. Analyzing security/privacy risks in Machine Learning (ML) models
- R2. Building tools for finding vulnerabilities in server/client-side web applications
- R3. Finding security/privacy vulnerabilities in web services
- R4. Analyzing online scam/criminal activities  occurring on the Internet

## Representative Works
{% for item in site.research.list %}

  {% if item.photo %}
    <div class="photo"
         style="background:url({{item.photo}}) left no-repeat; background-size:contain;">
  {% endif %}
  <ul>
    <li> {{item.subject}} </li>
    {% for title in item.title %}
    <li>{{ title }}</li>
    {% endfor %}
    {% if item.contents %}
    <li>
      {% if item.media %}
      [<a href="{{ item.media }}">]media</a>]
      {% endif %}
      {% if item.paper %}
      [<a href="{{ item.paper }}">]paper</a>]
      {% endif %}
      {% if item.code %}
      [<a href="{{ item.code }}">]code</a>]
      {% endif %}
      {% if item.summary %}
      [<a href="{{ item.summary }}">]summary</a>]
      {% endif %}
    </li>
  {% endif %}
{% endfor %}

<!--
<div class="posts">
  {% for post in site.posts %}
    <article class="post">
-->
<!--
      <h3><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h3>
      <div class="entry">
        {{ post.excerpt }}
      </div>
-->
<!--
      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
      -->
<!--
    </article>
  {% endfor %}
</div>
-->
