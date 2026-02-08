{%- include ui.html %}
{%- assign _tjw_page = page.url | slice: 0, 21 %}
{%- assign _page_path = page.path | slice: _tjw_page.size, page.path.size %}
{%- if page.use_header == false %}
<style>._header{display:none !important}</style>
{%- elsif _tjw_page == '/techie-joe.github.io' %}

{%- case _page_path %}
{%- when 'index.md' %}
{%- include logo.html %}
{%- else %}
{%- include tjw_logo.html %}
{%- endcase %}

{%- else %}

{%- case page.path %}
{%- when 'index.md' %}
{%- include dove/tj_logo.html %}
{%- else %}
{%- include logo.html %}
{%- endcase %}

{%- endif %}