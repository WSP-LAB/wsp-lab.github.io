---
layout: main
---
<div class="text-center">
<img src="images/main_wordcloud.svg">
</div>
---
## News
<ul>
{% for item in site.news.list %}
  <li>
    <i class="fas fa-paper-plane"><strong>&nbsp;{{item.date}}</strong></i>:&nbsp;{{ item.comments }}
  </li>
{% endfor %}
</ul>
---
<div style="text-align: center">
  <div class="row">
    <div class="col-md-3"></div>
    <div class="col-md-6">
      <a href="https://gsis.kaist.ac.kr/"><img src="images/kaist-gsis.png" style="width:400px;" /></a>
    </div>
    <div class="col-md-3"></div>
  </div>
</div>
