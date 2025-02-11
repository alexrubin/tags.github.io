---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: tags
---

{% comment %} <h2>Tag List</h2> {% endcomment %}

<div>
    <input type="text" id="myInput" onkeyup="myFunction()" placeholder="Search...">
</div>

<ul id="tagList">
{%- for t in site.data.tags -%}
    <li>{% if t.url %}<a href="{{ t.url }}" target="_blank">{% endif %}{{ t.title }}{% if t.url %}</a>{% endif %}{% if t.pitch %} - {{ t.pitch }}{% endif %}{% if t.arranger %}<em> ({{ t.arranger }})</em>{% endif %}</li>
{%- endfor -%}
</ul>