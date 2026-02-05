---
use_header: false
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

{{ thin_hr }}

### We are testing

[Techie Joe's Website](techie-joe.github.io)

### Pages

{% include pages.md %}

### Related Projects

[Dove](https://techie-joe.github.io/dove){: target="techie-joe.github.io/dove" }

<div style="margin-top:1rem"></div>

{% comment %} --- end of page --- {% endcomment %}