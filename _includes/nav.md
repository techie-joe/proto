{%- include ui.html %}
{%- assign _tjw_page = page.url | slice: 0, 21 %}
{%- if page.use_nav == false -%}
<style>._nav{display:none !important}</style>
{%- elsif _tjw_page == '/techie-joe.github.io' %}

{%- include tjw_nav.md %}
{{ thin_hr }}

{%- else %}

{%- include proto_nav.md %}
{{ thin_hr }}

{%- endif %}
{% comment %} --- end of page --- {% endcomment %}