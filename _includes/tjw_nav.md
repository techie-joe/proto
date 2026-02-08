{%- assign _path = page.path %}
{%- assign _tjw_page = page.url | slice: 0, 21 %}
{%- assign _page_path = page.path | slice: _tjw_page.size, page.path.size %}
{%- if _page_path == 'index.md' -%}
**Home**{%- else -%}[Home]({{ site.home_url }}{{ _tjw_page }}/)
{%- endif %}