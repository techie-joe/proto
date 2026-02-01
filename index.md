---
use_nav: false
---
{% include ui.html %}

<div class="relative"><div class="_bimoji">🚧</div></div>

<h1 id="{{ site.title | downcase | append:'site' | replace:' ','-' }}">🚧 {{ site.title }} site</h1>
{: style="border:0" }

```yml
version        : {{ site.version | default: '(undefined)' }}
revision       : {{ site.revision | default: '(undefined)' }}
build_revision : {{ site.github.build_revision | default: '(undefined)' }}
```
{: style="max-width:600px" }

### Pages

{% include pages.md %}

### Projects

- [Dove](https://techie-joe.github.io/dove){: target="techie-joe.github.io/dove" }

<div style="margin-top:3rem"></div>

{% comment %} --- end of page --- {% endcomment %}