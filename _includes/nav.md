{%- include ui.html %}
{%- if page.use_nav == false -%}
<style>._nav{display:none !important}</style>
{%- else %}

<!-- your nav goes here -->

{%- if page.path == 'index.md' -%}
**Home**{%- else -%}[Home]({{ site.home_url }}/)
{%- endif %}
{{- bull -}}
{%- if page.path == 'about.md' -%}
**About**{%- else -%}[About]({{ site.baseurl }}/about)
{%- endif %}
{{- bull -}}
{%- if page.path == 'pages.md' -%}
**Pages**{%- else -%}[Pages]({{ site.baseurl }}/pages)
{%- endif %}
{{- bull -}}
{%- if page.path == 'posts.md' -%}
**Posts**{%- else -%}[Posts]({{ site.baseurl }}/posts)
{%- endif %}

{{ thin_hr }}

{%- endif %}
{% comment %} --- end of page --- {% endcomment %}