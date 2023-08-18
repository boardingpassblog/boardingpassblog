---
layout: section
title: Opinión
permalink: /opinion/
---

{% 
  include ads/banner.html 
  content=site.data.ads.section-opinion 
%}

{% include pages/title.html %}

<!-- blog post -->
<section class="section">
  <div class="container maxw">
    <div class="row">
      <div class="col-lg-9">
        {% for post in site.posts %}
        {% if post.categories contains 'opinion' %}
        {% capture thecycle %}{% cycle 'odd', 'even' %}{% endcapture %}
        {% if thecycle == 'odd' %}
        {% assign class = '' %}
        {% else %}
        {% assign class = 'article-right' %}
        {% endif %}
          {% include pages/article.html %}
        {% endif %}
        {% endfor %}
      </div>
      <div class="col-lg-3">
        {% 
          include ads/banner.html 
          content=site.data.ads.sidebar_opinion-0
        %}
        {% include destacado.html %}
        {% 
          include ads/banner.html 
          content=site.data.ads.sidebar_opinion-1  
        %}
        {% include recientes.html %}
        {% 
          include ads/banner.html 
          content=site.data.ads.sidebar_opinion-2
        %}
        {% include secciones.html %}
        {% 
          include ads/banner.html 
          content=site.data.ads.sidebar_opinion-3
        %}
      </div> 
    </div>
  </div>
</section>
<!-- /blog post -->