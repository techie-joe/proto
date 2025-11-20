---
title: Liquid basics
description: Basic Liquid syntaxes on this site.
---
# {{ page.title }}

###### strings

```liquid
{% raw %}{% assign var = value_or_expression | filter: 'filter_expression' %}{% endraw %}
```

```yml
var     : {{ var | default: '(value_or_expression)' }}
default : {{ undefined | default: '(undefined)' }}
nil     : {{ nil | default: '(nil is false and renders nothing)' }}
```

{% assign string   = 'jAmEs r pEtErSoN' %}
{% assign color    = 'blue' %}

```yml
string        : {{ string }} [{{ string | size | append: ' characters' }}]
upcase        : {{ string | upcase }}
downcase      : {{ string | downcase }}
capitalize    : {{ string | capitalize }}
replace       : {{ string | capitalize | replace: "peterson", "Rodney" }}
truncate      : {{ string | truncate: 7 }}
# remove 'r'  : {{ string | remove: 'r' }}
# remove 'r ' : {{ string | remove: 'r ' }}

color : {{ color }}{{' > '}}{% assign color = "green" %}{{ color }}
```

###### date

{% assign date     = '2005-03-09T20:10:30' %}

```yml
date : {{ date }}
date : {{ date | date: "%A, %B %d, %Y @ %I:%M:%S %p" }}
```

| -- | :-------------------------------- | ----- | 
| %B | Full month name | November |
| %b | Abbreviated month name | Nov |
| %A | Full day name | Thursday |
| %a | Abbreviated day name | Thursday |
| %w | Day of the week as a number (0=Sunday, 6=Saturday) | 4 |
| %d | Month as a padded number (01-12) | 03 |
| %m | Month as a padded number (01-12) | 03 |
| %Y | Full year (4 digits) | 2005 |
| %y | Year as a padded number (2 digits) | 05 |
| %H | 24-hour clock (00-23) | 21 |
| %I | 12-hour clock (01-12) | 06 |
| %M | Minute as a padded number (00-59) | 01 |
| %S | Second as a padded number (00-59) | 02 |
| %p | AM/PM indicator (uppercase) | PM |
{: .simple }

###### controls

```
if true : {% if true -%}then{%- endif %}
elsif true : {% if false -%}{%- elsif true -%}then{%- endif %}
else : {% if false -%}{%- else -%}means (others){%- endif %}

unless false : {% unless false %}means (other than false){%- endunless %}

case 'a' : {% case 'a' -%}
{%- when 'a' -%}is A
{%- endcase %}
```

###### loops

```liquid
{% raw %}{% for i in (1..9) limit:5 -%}{{ i }}{% cycle 'odd', 'even' %}{%- endfor %}{% endraw %}
```

```
{% for i in (1..9) limit:5 -%}{{ i }}{{' '}}{%- endfor %}
```

> Use {% raw %}`{% break %}` and `{% continue %}` to get out of a loop.{% endraw %}

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

{% comment %}
###### misc
{% if '' == blank %}Check a blank string with the `blank` object.{%- endif %}
{% if undefined == empty %}Compare with `empty` to check whether an object exists before accessing any of its attributes.{%- endif %}
{% endcomment %}
