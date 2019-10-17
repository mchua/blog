---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
<ul class="posts">
  <span>Articles</span>
  {% for post in site.posts %}
    {% unless post.next %}
    <div class="line"><span>{{ post.date | date: '%Y' }}</span></div>
    {% else %}
      {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
      {% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
      {% if year != nyear %}
        <div class="line"><span>{{ post.date | date: '%Y' }}</span></div>
      {% endif %}
    {% endunless %}

    <li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
