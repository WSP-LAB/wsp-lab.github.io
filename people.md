---
layout: default
---

## Professor
<div class="row">
  <div class="col-md-4"></div>
  <div class="col-md-4 namecard">
    <table style="width: 320px; margin: 0 auto;">
      <tr>
        <td>
        {% if site.people_prof.photo %}
                  <div class="photo"
                       style="background:url({{ site.people_prof.photo }}) center no-repeat; background-size:contain;">
        {% else %}
                  <div class="photo"
                     style="background:url(/images/user.svg) center no-repeat; background-size:contain;">
        {% endif %}
          </div>
        </td>
        <td class="container">
        {{ site.people_prof.name }}<br />
        <em>Professor</em><br />
        <a href="{{ site.people_prof.homepage }}">
          <span class="glyphicon glyphicon-home"></span> [homepage]
        </a>
        </td>
      </tr>
    </table>
  </div>
  <div class="col-md-4"></div>
</div>

{% if site.people_phd %}
---
## Ph.D. Students
{% for person in site.people_phd %}
{% assign mod3 = forloop.index | modulo: 3 %}
{% if mod3 == 1 %}
<div class="row">
{% endif %}
  <div class="col-md-4 namecard">
    <table>
      <tr>
        <td>
{% if person.photo %}
          <div class="photo"
               style="background:url({{ person.photo }}) center no-repeat; background-size:contain;">
{% else %}
          <div class="photo"
             style="background:url(/images/user.svg) center no-repeat; background-size:contain;">
{% endif %}
          </div>
        </td>
        <td class="container">
          {{ person.name }}<br />
          <em>Ph.D. Student</em>
          {% if person.homepage %}
          <br />
          <a href="{{ person.homepage }}">
            <span class="glyphicon glyphicon-home"></span> [homepage]
          </a>
        {% endif %}
        </td>
      </tr>
    </table>
  </div>
{% if mod3 == 0 or forloop.last == true %}
</div>
{% endif %}
{% endfor %}
{% endif %}

{% if site.people_master %}
---
## Master Students
{% for person in site.people_master %}
{% assign mod3 = forloop.index | modulo: 3 %}
{% if mod3 == 1 %}
<div class="row">
{% endif %}
  <div class="col-md-4 namecard">
    <table>
      <tr>
        <td>
{% if person.photo %}
          <div class="photo"
               style="background:url({{ person.photo }}) center no-repeat; background-size:contain;">
{% else %}
          <div class="photo"
             style="background:url(/images/user.svg) center no-repeat; background-size:contain;">
{% endif %}
          </div>
        </td>
        <td class="container">
          {{ person.name }}<br />
          <em>Master Student</em>
          {% if person.homepage %}
          <br />
          <a href="{{ person.homepage }}">
            <span class="glyphicon glyphicon-home"></span> [homepage]
          </a>
        {% endif %}
        </td>
      </tr>
    </table>
  </div>
{% if mod3 == 0 or forloop.last == true %}
</div>
{% endif %}
{% endfor %}
{% endif %}

{% if site.people_intern %}
---
## Interns
{% for person in site.people_intern %}
{% assign mod3 = forloop.index | modulo: 3 %}
{% if mod3 == 1 %}
<div class="row">
{% endif %}
  <div class="col-md-4 namecard">
    <table>
      <tr>
        <td>
{% if person.photo %}
          <div class="photo"
               style="background:url({{ person.photo }}) center no-repeat; background-size:contain;">
{% else %}
          <div class="photo"
             style="background:url(/images/user.svg) center no-repeat; background-size:contain;">
{% endif %}
          </div>
        </td>
        <td class="container">
          {{ person.name }}<br />
          <em>Intern</em>
          {% if person.homepage %}
          <br />
          <a href="{{ person.homepage }}">
            <span class="glyphicon glyphicon-home"></span> [homepage]
          </a>
        {% endif %}
        </td>
      </tr>
    </table>
  </div>
{% if mod3 == 0 or forloop.last == true %}
</div>
{% endif %}
{% endfor %}
{% endif %}

{% if site.people_researcher %}
---
## Researchers
{% for person in site.people_researcher %}
{% assign mod3 = forloop.index | modulo: 3 %}
{% if mod3 == 1 %}
<div class="row">
{% endif %}
  <div class="col-md-4 namecard">
    <table>
      <tr>
        <td>
{% if person.photo %}
          <div class="photo"
               style="background:url({{ person.photo }}) center no-repeat; background-size:contain;">
{% else %}
          <div class="photo"
             style="background:url(/images/user.svg) center no-repeat; background-size:contain;">
{% endif %}
          </div>
        </td>
        <td class="container">
          {{ person.name }}<br />
          <em>Researcher</em>
          {% if person.homepage %}
          <br />
          <a href="{{ person.homepage }}">
            <span class="glyphicon glyphicon-home"></span> [homepage]
          </a>
        {% endif %}
        </td>
      </tr>
    </table>
  </div>
{% if mod3 == 0 or forloop.last == true %}
</div>
{% endif %}
{% endfor %}
{% endif %}

{% if site.people_alumni %}
---
## Alumni
<ul>
{% for person in site.people_alumni %}
{% if person.homepage %}
  <li class="alumni_item"><a href="{{ person.homepage }}">{{ person.name }}</a>, {{ person.degree }}, now at {{ person.work }}.</li>
{% else %}
  <li class="alumni_item">{{ person.name }}, {{ person.degree }}, now at {{ person.work }}.</li>
{% endif %}
{% endfor %}
</ul>
{% endif %}
