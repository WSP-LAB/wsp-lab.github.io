---
layout: default
---

## Research Area
WSP Lab(Web Security & Privacy Lab) has a vision, `Be more secure on the Web`, and they are working with the goal of detecting vulnerabilities and measuring privacy violations occurring on the Web.
Our research area includes:
- Detection web service vulnerabilities through dynamic/static analysis
- Review of a functionality security on a web browser
- Discovery of security vulnerabilities with machine learning
- Detection and analysis of service abusing in web/mobile service

## Representative Works
<div class="posts">
  {% for post in site.posts %}
    <article class="post">

      <h3><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h3>

      <div class="entry">
        {{ post.excerpt }}
      </div>

      <!--
      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
      -->
    </article>
  {% endfor %}
</div>
