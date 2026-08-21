---
layout: main
---
<div class="text-center">
<img src="images/main_wordcloud.svg">
</div>
---
## News
<ul id="news-list">
{% for item in site.news.list %}
  <li{% if forloop.index > 15 %} class="news-hidden" style="display: none;"{% endif %}>
    <i class="fas fa-paper-plane"><strong>&nbsp;{{item.date}}</strong></i>:&nbsp;{{ item.comments }}
  </li>
{% endfor %}
</ul>
{% if site.news.list.size > 15 %}
<div class="news-more-wrap">
  <button id="news-more-btn" type="button" class="btn-more">More&nbsp;&nbsp;&#8595;</button>
</div>
<script>
  document.getElementById('news-more-btn').addEventListener('click', function () {
    var hidden = document.querySelectorAll('#news-list .news-hidden');
    for (var i = 0; i < hidden.length && i < 15; i++) {
      hidden[i].style.display = '';
      hidden[i].classList.remove('news-hidden');
    }
    if (document.querySelectorAll('#news-list .news-hidden').length === 0) {
      this.style.display = 'none';
    }
  });
</script>
{% endif %}
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
