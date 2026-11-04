---
title: "Huang Lab - Team"
layout: gridlay
excerpt: "Huang Lab: Team members"
sitemap: false
permalink: /team/
---

# Group Members

 **We are  looking for new Postdocs, PhD students and Master students to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/vacancies) **!**


Staff
{% assign number_printed = 0 %} {% assign fac_array = site.data.team.faculty | sort: "lastname" %} {% for member in fac_array %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}

{% endif %}
{% if member.social.website %}

{% if member.photo %}  {% endif %}

{{ member.name }}
{% else %}
{% if member.photo %}  {% endif %}

{{ member.name }}
{% endif %}

{%- include socialmedia.html -%} {{ member.info }}

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %} {% if even_odd == 1 %}

{% endif %}
Current Students
{% assign number_printed = 0 %} {% assign stud_array = site.data.team.current-students | sort: "lastname" %}

{% for member in stud_array%}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}

{% endif %}
{% if member.social.website %}

{% if member.photo %}  {% endif %}

{{ member.name }}
{% else %}
{% if member.photo %}  {% endif %}

{{ member.name }}
{% endif %}

{%- include socialmedia.html -%} {{ member.info }} {% if member.advisor.size == 1 %} Advisor: {{ member.advisor }} {% endif %}

{% if member.advisor.size > 1 %} Advisor: {{ member.advisor[0] }}, {{ member.advisor[1] }} {% endif %}

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %} {% if even_odd == 1 %}

{% endif %}
{% if site.data.team.other-students.size > 0 %}

Students
{% endif %} {% assign number_printed = 0 %} {% for member in site.data.team.other-students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}

{% endif %}
{{ member.name }}
{{ member.info }}
{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %} {% if even_odd == 1 %}

{% endif %}
{% if site.data.team.visitor.size > 0 %}


Alumni
{% for member in site.data.alumni %}
{{ member.name }}
{{ member.role }}
{% endfor %}


