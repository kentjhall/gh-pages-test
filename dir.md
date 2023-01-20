# test16
{% assign doclist = site.static_files %}
<ul>
{% for doc in doclist %}
    {% unless doc.extname == '.md' or doc.extname == '.jpg' or doc.extname == '.png' or doc.extname == '.css' %}
    	{% if doc.path contains page.dir %}
	    <li><a href="{{ site.baseurl }}{{ doc.path }}">{{ doc.name }}</a></li>
        {% endif %}
    {% endunless %}
{% endfor %}
</ul>
