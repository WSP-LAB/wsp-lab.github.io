---
layout: default
---

## Research Area
Web Security & Privacy (WSP) Lab looks at security and privacy shortcomings in
complex software services including Web applications. Building automatic tools
for finding such shortcomings is the main research goal of our lab. The vision
of WSP lab is to find and implement novel ideas to make software services more
secure and private. Our research interests include the following areas:
- General topics in Web security/privacy
- Static and dynamic analysis in finding vulnerabilities
- Machine learning applications in security
- Security of machine learning models
- Side-channel attacks
- Web authentication

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
