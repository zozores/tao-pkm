{% for stream_name, stream_posts in group(kind="stream") %}
{% if stream_name == "notas" %}
##### últimas notas
<ul>
{% for post in stream_posts | slice(end=3) %}
<li><a href="{{ post.slug }}.html">{{ post.title }}</a></li>
{% endfor %}
</ul>
{% endif %}
{% if stream_name == "english" %}
##### latest posts in 🇬🇧
<ul>
{% for post in stream_posts | slice(end=3) %}
<li><a href="{{ post.slug }}.html">{{ post.title }}</a></li>
{% endfor %}
</ul>
{% endif %}
{% endfor %}
