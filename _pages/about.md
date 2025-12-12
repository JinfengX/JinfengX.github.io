---
permalink: /
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Welcome!
=====
{: #home }

I am Jinfeng Xu, currently a Ph.D. candidate in Computer Science at [Huazhong University of Science and Technology (HUST)](https://english.hust.edu.cn/), advised by [Prof. Xianzhi Li](https://nini-lxz.github.io/). Prior to my Ph.D. studies, I received my B.Eng. degree in Automation from [Shandong University](https://www.en.sdu.edu.cn/).

My current research centers on 3D computer vision, with a focus on point cloud semantic segmentation, open-world 3D scene understanding, and robust 3D perception in complex environments.. I am dedicated to developing generalizable learning frameworks that leverage large-scale models and data-efficient training to overcome the challenges of limited supervision in 3D domains.

I welcome research collaborations and interdisciplinary discussions related to 3D perception and open-world intelligence, and I am actively seeking postdoctoral opportunities to further develop cutting-edge research in these areas.

## News
{: #news }
{% if site.data.news %}
<div class="news-scroller" role="region" aria-label="News">
  <ul>
    {% for item in site.data.news %}
      <li>{{ item.text }}</li>
    {% endfor %}
  </ul>
  <div class="news-hint" aria-hidden="true">scroll for more &darr;</div>
</div>
{% endif %}


## Publications [[Google Scholar](https://scholar.google.com.hk/citations?user=qsJCXFoAAAAJ&hl=en)]
{: #publications }
{% assign pubs = site.data.publications %}
{% if pubs %}
<div class="pub-gallery">
  {% for pub in pubs %}
  {% assign has_image = pub.image | default: '' | strip %}
  {% if has_image != '' %}
  <article class="pub-card">
    <a class="pub-card__media" href="{{ pub.paper | default: pub.code | default: pub.project }}" target="_blank" rel="noopener">
      <img src="{{ pub.image | relative_url }}" alt="{{ pub.title }}">
    </a>
    <div class="pub-card__body">
      <div class="pub-list__title">
        {% if pub.paper %}
        <a href="{{ pub.paper }}" target="_blank" rel="noopener">{{ pub.title }}</a>
        {% else %}
        {{ pub.title }}
        {% endif %}
      </div>
      <div>{{ pub.authors }}</div>
      <div><em>{{ pub.venue }}</em></div>
      {% if pub.note %}<div>{{ pub.note }}</div>{% endif %}
      {% if pub.paper or pub.code or pub.project %}
        <div>
          {% if pub.paper %}[<a href="{{ pub.paper }}" target="_blank" rel="noopener">Paper</a>]{% endif %}
          {% if pub.code %}[<a href="{{ pub.code }}" target="_blank" rel="noopener">Code</a>]{% endif %}
          {% if pub.project %}[<a href="{{ pub.project }}" target="_blank" rel="noopener">Project</a>]{% endif %}
        </div>
      {% endif %}
    </div>
  </article>
  {% endif %}
  {% endfor %}
</div>
{% endif %}

{% assign has_text_only = false %}
{% for pub in pubs %}
  {% unless pub.image %}
    {% assign has_text_only = true %}
  {% endunless %}
{% endfor %}

{% if has_text_only %}
### Additional Publications
<ul>
  {% for pub in pubs %}
    {% unless pub.image %}
    <li>
      <div>
        {% if pub.paper %}
        <a href="{{ pub.paper }}" target="_blank" rel="noopener">{{ pub.title }}</a>
        {% else %}
        {{ pub.title }}
        {% endif %}
      </div>
      <div>{{ pub.authors }}</div>
      <div><em>{{ pub.venue }}</em></div>
      {% if pub.note %}<div>{{ pub.note }}</div>{% endif %}
      {% if pub.paper or pub.code or pub.project %}
        <div>
          {% if pub.paper %}[<a href="{{ pub.paper }}" target="_blank" rel="noopener">Paper</a>]{% endif %}
          {% if pub.code %}[<a href="{{ pub.code }}" target="_blank" rel="noopener">Code</a>]{% endif %}
          {% if pub.project %}[<a href="{{ pub.project }}" target="_blank" rel="noopener">Project</a>]{% endif %}
        </div>
      {% endif %}
    </li>
    {% endunless %}
  {% endfor %}
</ul>
{% endif %}

## Education
{: #education }

* **Huazhong University of Science and Technology**
  * Ph.D. in Computer Science, Sep. 2020 - Present
  * Advisor: [Prof. Xianzhi Li](https://nini-lxz.github.io/)
  * Research Topic: Open-World 3D Scene Understanding
* **Shandong University**
  * B.E. in Automation, Sep. 2016 – Jun. 2020 
  * Advisor: Prof. Xiaolei Li  
  * Thesis Title: Knowledge Graph–Based Personalized Recommendation System

## Honors & Awards
{: #honors-awards }

* Huawei Scholarship, 2024  
* Ph.D. First-Class Academic Scholarship, 2021–2024  
* National Special Prize, National Engineering Training Competition (Robotics), 2019  