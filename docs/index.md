---
title: Home
layout: home
---

# OSU Online CS Tools Information
<div>
{% if site.data.toc.toc[0] %}
  {% for item in site.data.toc.toc %}
    <h3>{{ item.title }}</h3>
      {% if item.subfolderitems[0] %}
        <ul>
          {% for entry in item.subfolderitems %}
            {% if entry.url %}
                <li><a href="{{ entry.url }}">{{ entry.page }}</a>
            {% else %}
                <li><span>{{ entry.page }}</span>
            {% endif %}
                    {% if entry.subsubfolderitems[0] %}
                    <ul>
                    {% for subentry in entry.subsubfolderitems %}
                        {% if subentry.url %}
                            <li><a href="{{ subentry.url }}">{{ subentry.page }}</a></li>
                        {% else %}
                            <li><span>{{ subentry.page }}</span>
                        {% endif %}
                    {% endfor %}
                    </ul>
                    {% endif %}
                </li>
          {% endfor %}
        </ul>
      {% endif %}
    {% endfor %}
{% endif %}
</div>