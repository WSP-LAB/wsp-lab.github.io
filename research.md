---
layout: default
---
<style>
  div.row {
    width: 90%
    display: flex;
  }
  
  div.left {
    width: 30%;
    float: left;
  }  
  
  div.left {
    width: 40%;
    float: right;
  }
</style>


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
{% for article in site.research %}
  <strong> {{ article.subject }} </strong>
  
  <div class="row">
  {% for item in article.list %}
    {% if item.photo %} 
      <div class="left">
        <img src = "{{item.photo}}" width="100%">
      </div>
    {% endif %}
    
  <div class="right">
    {% for title in item.title %}
      <strong>{{ title }}</strong>
    {% endfor %}
    {% if item.contents %}
      <li>{{ item.contents }}</li>
      
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
          <br>
        {% endif %}
        <br>
        
   </div>
    

  
  {% endif %}
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
