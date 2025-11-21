---
title: Handling list
description: Handling list using Liquid.
---
# {{ page.title }}

{% assign list_x   = 'a,m,b,n,c,o,z,y,x' | split: ',' %}
{% assign sorted_list_x = list_x | sort %}
{% assign reverse_sorted_list_x = list_x | sort | reverse %}
{% assign sliced_sorted_list_x  = sorted_list_x | slice: 3, 3 %}

```yml
list_x   : {{ list_x }} [{{ list_x | size | append: ' items' }}]
jsonify  : {{ list_x | jsonify }}
join     : {{ list_x | join: ',' }}
order    : {{ list_x | first }}{{' ... '}}{{ list_x | last }}
loop     : # {% for item in list_x %}[{{ item }}]{{' '}}{%- endfor %}
sort     : {{ list_x | sort | jsonify }}
reverse  : {{ list_x | reverse | jsonify }}
slice    : {{ list_x | sort | slice: 3, 3 | jsonify }}
```

{% assign list_a = 'apple,banana,cherry' | split: ',' %}

```yml
list_a   : {{ list_a | jsonify }} [{{ list_a | size | append: ' items' }}]
```

{% assign list_a = list_a | join: ',' | prepend: 'pear,' | append: ',durian' | split: ',' %}

```yml
list_a   : {{ list_a | jsonify }} [{{ list_a | size | append: ' items' }}]
```

{% assign list_b   = '["pen","gum","tin"]' | parse_json %}

```yml
list_b   : {{ list_b }} [{{ list_b | size | append: ' items' }}]
jsonify  : {{ list_b | jsonify }}

{{'# '}}{% for item in list_b %}[{{ item }}]{{' '}}{%- endfor %}
```

{% assign products = '[
  "laptop"   => {"name": "Ace",  "price": 1200.00, "in_stock": true},
  "mouse"    => {"name": "Mice", "price": 25.50,   "in_stock": true},
  "keyboard" => {"name": "Keys", "price": 80.90,   "in_stock": false}
]' | parse_json %}

```yml
products         : {{ products | jsonify }} [{{ products | size | append: ' items' }}]

{{'# '}}{% for item in products limit:2 %}[{{ item }}],
{%- endfor %}
```