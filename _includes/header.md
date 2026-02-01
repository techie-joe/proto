{%- include ui.html %}
{%- if page.use_header == false %}
<style>._header{display:none !important}</style>
{%- else %}

{%- if page.path == 'index.md' %}
{%- include tj_logo.html %}
{%- else %}
{%- include logo.html %}
{%- endif %}

{%- endif %}