---
index: false
layout: mallet
title: Techie Joe's Website
description: Hand picked tools and resources.
# use_header: false
use_nav: false
---
{% include ui.html %}

<div class="relative"><div class="_bimoji">🖥️</div></div>

<div style="margin-top:3rem"></div>

# {{ page.title }}

🛠️ **{{ page.description | remove:'.' }}**

I build apps and tools to make development faster and smarter. Dive in to see what I’m working on or check out my library of tools below!
{: .text-justify style="max-width:450px" }

{%- capture _links %}

[Techie Joe's Code Library][library]{: .button.primary }{{''-}}
[Ace][ace]{: .button }{{''-}}
[Nova][nova]{: .button }{{''-}}
[Dove][dove]{: .button }{{''-}}
[Mallet][mallet]{: .button }

[library]: https://techie-joe.github.io/library "Techie Joe's Code Library - A treasure trove for curious coders and wondering enthusiast."
[ace]:     https://techie-joe.github.io/ace "Ace Builder - A power-tool for building websites and web applications."
[nova]:    https://techie-joe.github.io/nova "Nova - Simple framework for websites and web applications."
[dove]:    https://techie-joe.github.io/dove "Dove - Jekyll theme development project."
[themejs]: https://techie-joe.github.io/themejs "ThemeJs - A toggle switch for multi-theme websites."
[mallet]:  https://techie-joe.github.io/mallet "Techie Joe's Mallet is a Jekyll theme for GitHub Pages."
[prime]:   https://techie-joe.github.io/prime "Techie Joe's Prime is a Jekyll theme for GitHub Pages."

{%- endcapture %}
<style> #_links { max-width:600px } </style>
<div id="_links">{{ _links | markdownify }}</div>

<div style="margin-top:3rem"></div>

###### 👋 Welcome to my workshop!

{{ thin_hr }}

After two decades of engineering, I stopped reinventing solutions and started systematizing them. This is where those solutions live. In this curated collection of resources, you’ll find practical development practices, articles, tools, frameworks, and design principles to build cleaner, faster and smarter websites and applications. Find out what suits you, and let's build something great together.

- **Maintained Tools** — Libraries and frameworks I actively use.
- **Engineering Patterns** — Practical architecture and clean-code principles.
- **Workflow Accelerators** — Utilities and AI-assisted processes that remove friction.

<div style="margin-top:3rem"></div>

###### 📝 _Blog Articles_

{{ thin_hr }}

**[The Developer's Launch Sequence](hello-world)** &mdash; For most people, **"Hello World"** is just a phrase that's totally basic, maybe even a little cliche. But if you're actually building things, those two tokens are the real starting point. The second they render correctly on my screen, the portal swings wide open. That's the moment I can confidently confirm that the machine is listening. [Read more ..](hello-world)

<div style="margin-top:3rem"></div>