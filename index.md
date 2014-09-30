---
layout: default
---

<div>
	{% for category in  site.categories  %}
        <h2 id="{{ category | first }}">{{ category | first | capitalize}}</h2>
        {% assign cat = category | first %}
        {% for post in site.posts %}
        	{% if post.category == cat %}
			<ul class="widget">
				<li><a href="/{{ post.permalink }}">{{ post.title }}</a></li>
			</ul>
			{% endif %}	
		{% endfor %}
	{% endfor %}
</div>