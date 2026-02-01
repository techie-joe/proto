{%- include ui.html %}
{%- if page.use_header == false %}
<style>._header{display:none !important}</style>
{%- else %}

<!-- your header goes here -->
{%- case page.path %}
{%- when 'index.md' %}
{%- include dove/tj_logo.html %}
{%- else %}
{%- include logo.html %}
{%- endcase %}

{%- endif %}