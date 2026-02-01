{%- include ui.html %}
{%- if page.use_nav == false -%}
<style>._nav{display:none !important}</style>
{%- else %}
{%- include dove/nav.md %}
{%- endif %}
{% comment %} --- end of page --- {% endcomment %}