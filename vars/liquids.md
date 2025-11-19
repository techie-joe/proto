---
title: Liquid
description: Liquid on this site.
use_nav: false
use_footer: false
---
# {{ page.title }}

###### comments

There’s a comment block below this line.

<!-- This HTML comment will not appear in the rendered Markdown -->

{% comment %}This Liquid comment will not appear in the rendered Markdown{% endcomment %}

Comment block should not appear in the rendered Markdown.

###### capture

{% capture block %}
> **captured block**{: .text-purple }
{%- endcapture %}

{{ block }}

###### raw

{% raw %}{% raw %}... {% endraw %}{%- endraw %}

###### controls

```
{% echo 'echo' %}

{% assign condition = 'yes' %}
{% if condition %}
if.condition :{{ condition }}
{%- endif %}

{% assign condition_2 = 'no' %}
{% if condition_ %}
{%- elsif condition_2 %}
elsif.condition_2 :{{ condition_2 }}
{%- endif %}

{% assign condition_3 = 'idk' %}
{% if condition_ %}
{%- else %}
else.condition_3 :{{ condition_3 }}
{%- endif %}

{% assign condition_4 = 'unique' %}
{% unless condition_4 == 'unique' %}condition_4 :{{ condition_4 }}{%- endunless %}

{% assign condition_5 = 'when' %}
{% case condition_5 %}
case.condition_5 :
{%- when 'when' %}{{ condition_5 }}
{%- endcase %}
```

###### loop

```
{% assign collection = [3,4,6,7] %}
{% for item in collection %}{{ item }},{%- endfor %}

{% for item in collection %}
- {{ item }}
{%- endfor %}

# there is also break and continue.
```