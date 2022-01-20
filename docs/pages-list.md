---
layout: page
---

probably should be used for the nav bar..

 {% for page in site.pages %}
          <li><a href="{{ page.url }}">{{ page.title }}</a></li>
  {% endfor %}  <!-- page -->
