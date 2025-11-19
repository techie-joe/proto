---
title: Variables
use_nav: false
use_footer: false
---
# {{ page.title }}

```yml
layout        : {{ layout }}
title         : {{ title }}
description   : {{ description }}
```

```yml
site.title         : {{ site.title }}
site.description   : {{ site.description }}
```

```yml
page.title         : {{ page.title }}
page.description   : {{ page.description }}
```

{% assign nick = 'nik' %}
```yml
name : {{ name }}
nick : {{ nick }}
```