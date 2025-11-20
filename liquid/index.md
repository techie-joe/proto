---
title: Liquid
description: Liquid on this site.
use_nav: false
use_footer: false
---
# {{ page.title }}

###### assign values

```yml
# {% raw %}{% assign var = value_or_expression | filter: 'filter_expression' %}{% endraw %}
var     : {{ var | default: '(value_or_expression)' }}
default : {{ undefined | default: '(default)' }}
```

{% assign string   = 'jAmEs pEtErSoN' %}
{% assign color    = 'blue' %}

```yml
# string
string      : {{ string }}
string.size : {{ string | size }}
upcase      : {{ string | upcase }}
downcase    : {{ string | downcase }}
capitalize  : {{ string | capitalize }}
replace     : {{ string | capitalize | replace: "peterson", "Rodney" }}

# color
color : {{ color }}
color : {% assign color = "green" %}{{ color }}
```

###### list & loops

{% assign list_a   = 'apple,banana,cherry' | split: ',' %}

```yml
# list_a       = 'apple,banana,cherry'
list_a         : {{ list_a }}
list_a.size    : {{ list_a | size }}
list_a.jsonify : {{ list_a | jsonify }}
list_a.0       : {{ list_a[0] }}{% assign list_a[0] = "pear" %}{{' > '}}{{ list_a[0] }}
list_a.3       : {{ list_a[3] }}{% assign list_a[3] = "durian" %}{{' > '}}{{ list_a[3] }}
list_a.jsonify : {{ list_a | jsonify }}

{{'# '}}{% for item in list_a limit:3 %}[{{ item }}],
{%- endfor %}
```

{% assign list_b   = '["pen","gum","tin"]' | parse_json %}

```yml
# list_b       = '["pen","gum","tin"]'
list_b         : {{ list_b }}
list_b.size    : {{ list_b | size }}
list_b.jsonify : {{ list_b | jsonify }}
list_b.0       : {{ list_b[0] }}{% assign list_b[0] = "bin" %}{{' > '}}{{ list_b[0] }}
list_b.3       : {{ list_b[3] }}{% assign list_b[3] = "can" %}{{' > '}}{{ list_b[3] }}
list_b.jsonify : {{ list_b | jsonify }}

{{'# '}}{% for item in list_b limit:3 %}[{{ item }}],
{%- endfor %}
```

{% assign products = '[
  "laptop"   => {"name": "Ace",  "price": 1200.00, "in_stock": true},
  "mouse"    => {"name": "Mice", "price": 25.50,   "in_stock": true},
  "keyboard" => {"name": "Keys", "price": 80.90,   "in_stock": false}
]' | parse_json %}

```yml
# products = '[
# "laptop"   => {"name": "Ace",  "price": 1200.00, "in_stock": true},
# "mouse"    => {"name": "Mice", "price": 25.50,   "in_stock": true},
# "keyboard" => {"name": "Keys", "price": 80.90,   "in_stock": false}
# ]'
products         : {{ products }}
products.size    : {{ products | size }}
products.jsonify : {{ products | jsonify }}
products[0]      : {{ products[0] }}
products.laptop  : {{ products.laptop | jsonify }}

{{'# '}}{% for item in products limit:2 %}[{{ item }}],
{%- endfor %}
```

Use {% raw %}`{% break %}` and `{% continue %}` to get out of a loop.{% endraw %}

###### date

{% assign date     = '2025-11-19T20:10:30' %}

```yml
# date
date : {{ date }}
date : {{ date | date: "%B %d, %Y @ %h:%m:%s" }}
```

| -- | :-------------------------------- | ----- | 
| %B | Full month | November |
| %b | Abbreviated month | Nov |
| %m | Month as a padded number (01-12) | 03
| %Y | Full year (4 digits) | 2005
| %y | Year as a padded number (2 digits) | 05
| %H | 24-hour clock (00-23) | 21
| %I | 12-hour clock (01-12) | 06
| %M | Minute as a padded number (00-59) | 01
| %S | Second as a padded number (00-59) | 02
| %p | AM/PM indicator (uppercase) | PM
{: .simple }

###### controls

```
{% if true %}if{%- endif %}
{% if false %}{%- elsif true %}elsif{%- endif %}
{% if false %}{%- else %}else{%- endif %}
{% unless false %}unless false is true{%- endunless %}
{% case 'a' -%}
case:
{%- when 'a' %}is A
{%- when 'b' %}is B
{%- endcase %}
```

###### capture

{% capture block %}
**captured block**{: .text-purple }
{%- endcapture %}

{{ block }}
{: .box.ba.text-center }

###### comments

There’s a comment block below this line.

<!-- This HTML comment will not appear in the rendered Markdown -->

{% comment %}This Liquid comment will not appear in the rendered Markdown{%- endcomment %}
{% comment %}
in multiple
lines too
{%- endcomment %}

Comment block should not appear in the rendered Markdown.

###### raw

`raw` skips liquid rendering.
Be carefull using it. Closing with `%-` cause build error.  

```liquid
{% raw %}{% assign x = 'x' %}{% comment %}comment{% endcomment %}{% endraw %}
{% raw %}product.title : {{ product.title }}
product.description : {{ product.description }}{% endraw %}
```

###### echo

Github Pages does not support `echo` at the moment.

```liquid
{% raw %}{% echo 'echo' %}{% endraw %}
```

###### render

Github Pages does not support `render` at the moment. 

```liquid
{% raw %}{% render 'snippet', 
  card_title: "Coffee Maker", 
  card_description: "Brews perfect coffee every time." 
%}{% endraw %}
```
