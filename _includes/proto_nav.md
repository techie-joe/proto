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