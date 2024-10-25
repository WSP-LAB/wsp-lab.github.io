---
layout: default
---
<style>
.left-box {
  float: left;
  width: 50%;
  padding: 20px;
}

.right-box {
  float: right;
  width: 50%;
  padding: 10px;
  word-break:break-all;
  box-sizing:border-box;
}

</style>


## Research Area
<div>
Web Security & Privacy (WSP) Lab  conducts research on various topics regarding web
security and privacy. We envision making Internet services more secure and private
by contemplating novel ideas and implementing them in real-world services.
Our research topics can be categorized into four research directions:
</div>
- R1. Analyzing security/privacy risks in Machine Learning (ML) models
- R2. Building tools for finding vulnerabilities in server/client-side web applications
- R3. Finding security/privacy vulnerabilities in web services
- R4. Analyzing online scam/criminal activities  occurring on the Internet
<hr>
## Representative Works

  {% for article in site.research %}
  <p style="font-size:20px"><strong>
    {{ article.subject }}
  </strong></p>

  {% for item in article.list %}

  {% for title in item.title %}
  <div class="container">
  <strong>
    <i>{{ title }}</i>
  </strong>
  </div>
  {% endfor %}
  <div class="container">
  {% if item.photo %}
  {% if item.horizontal %}
  <br>
  <div>
    <img src = "{{item.photo}}">
  </div>
  <br>
  <div>
  {% else %}

  <div class='left-box'>
    <img src = "{{item.photo}}">
  </div>

  <div class='right-box'>
  {% endif %}
  {% else %}
  <div>
  {% endif %}

  {% if item.contents %}
  <li>{{ item.contents }}</li>
  {% endif %}
  {% if item.media %}
  <a href="{{ item.media }}">[media]</a>
  {% endif %}
  {% if item.paper %}
  <a href="{{ item.paper }}">[paper]</a>
  {% endif %}
  {% if item.code %}
  <a href="{{ item.code }}">[code]</a>
  {% endif %}
  {% if item.summary %}
  <a href="{{ item.summary }}">[summary]</a>
  {% endif %}
  {% if item.contents %}
  <br><br><br>
  {% endif %}
  </div></div>
  {% endfor %}


  {% if forloop.last == false %} <hr> {% endif %}
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
