{%- include ui.html %}
{%- if page.use_footer == false -%}
<style>._footer{display:none !important}</style>
{%- else %}

{{ thin_hr }}

<!-- your footer goes here -->

{%- unless page.path == 'pages.md'
        or page.path == 'posts.md'
        or page.path == 'about.md'
        or page.path contains 'techie-joe.github.io/' %}
{%- capture site_nav %}{%- include nav.md %}{%- endcapture %}
<nav class="_common_nav">{{ site_nav | markdownify }}</nav>
{%- endunless %}

{%- capture tj_nav %}{%- include dove/tj_nav.md %}{%- endcapture %}
<nav class="_common_nav">{{ tj_nav | markdownify }}</nav>

{%- endif %}