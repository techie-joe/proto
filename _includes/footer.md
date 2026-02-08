{%- include ui.html %}
{%- assign _tjw_page = page.url | slice: 0, 21 %}
{%- assign _page_path = page.path | slice: _tjw_page.size, page.path.size %}
{%- if page.use_footer == false -%}
<style>._footer{display:none !important}</style>
{%- elsif _tjw_page == '/techie-joe.github.io' %}

{{ thin_hr }}

{%- unless _page_path == '404.md'
        or _page_path == 'index.md'
        or _page_path == 'pages.md'
        or _page_path == 'posts.md' %}
{%- capture site_nav %}{%- include tjw_nav.md %}{%- endcapture %}
<nav class="_common_nav">{{ site_nav | markdownify }}</nav>
{{ thin_hr }}
{%- endunless %}

{%- capture tj_nav %}{%- include dove/tj_nav.md %}{%- endcapture %}
<nav class="_common_nav">{{ tj_nav | markdownify }}</nav>

{%- else %}

{{ thin_hr }}

{%- unless page.path == '404.md'
        or page.path == 'index.md'
        or page.path == 'pages.md'
        or page.path == 'posts.md' %}
{%- capture site_nav %}{%- include proto_nav.md %}{%- endcapture %}
<nav class="_common_nav">{{ site_nav | markdownify }}</nav>
{{ thin_hr }}
{%- endunless %}

{%- capture tj_nav %}{%- include dove/tj_nav.md %}{%- endcapture %}
<nav class="_common_nav">{{ tj_nav | markdownify }}</nav>

{%- endif %}