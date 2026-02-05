---
index: false
layout: mallet
title: Techie Joe's Website
# use_header: false
use_nav: false
---
{% include ui.html %}

<div class="relative"><div class="_bimoji">🖥️</div></div>

<div style="margin-top:3rem"></div>

# {{ page.title }}

🖥️ **Welcome to my Lab!**

I build scalable apps, clean systems, and AI-driven workflows. Dive in to see what I’m working on or check out my library of tools below! 🛠️
{: style="max-width:450px" }

<style>
  #_links { max-width:600px }
  #_links a {
    display:inline-block;
    padding:.25rem 1rem;
    border:1px solid;
    border-radius:.25rem;
    margin:.25rem;
  }
</style>

{%- capture _links %}

[Techie Joe's Code Library][library]
[Ace][ace]
[Nova][nova] 
[Dove][dove]
[Mallet][mallet]  

[library]: https://techie-joe.github.io/library "Techie Joe's Code Library - A treasure trove for curious coders and wondering enthusiast."
[ace]:     https://techie-joe.github.io/ace "Ace Builder - A power-tool for building websites and web applications."
[nova]:    https://techie-joe.github.io/nova "Nova - Simple framework for websites and web applications."
[dove]:    https://techie-joe.github.io/dove "Dove - Jekyll theme development project."
[themejs]: https://techie-joe.github.io/themejs "ThemeJs - A toggle switch for multi-theme websites."
[mallet]:  https://techie-joe.github.io/mallet "Techie Joe's Mallet is a Jekyll theme for GitHub Pages."
[sites]:   https://techie-joe.github.io/sites "Techie Joe's Sites is a Jekyll theme for GitHub Pages."

{%- endcapture %}
<div id="_links">{{ _links | markdownify }}</div>

<div style="margin-top:3rem"></div>

{{ thin_hr }}

###### _🧠 What is it about?_{: .text-secondary }

After two decades of engineering, I stopped reinventing solutions and started systematizing them. I’ve found that the best tools are the ones you build yourself. This space is where those solutions live:

- **Maintained Tools** — Libraries and frameworks I actively use.
- **Engineering Patterns** — Practical architecture and clean-code principles.
- **Workflow Accelerators** — Utilities and AI-assisted processes that remove friction.

Everything here is battle-tested in real projects. Take what’s useful, and let's build something great together.

<div style="margin-top:3rem"></div>

###### _📝 Blog Articles_{: .text-secondary }

{{ thin_hr }}

**[The Developer's Launch Sequence](hello-world)** &mdash; For most people, **"Hello World"** is just a phrase that's totally basic, maybe even a little cliche. But if you're actually building things, those two tokens are the real starting point. The second they render correctly on my screen, the portal swings wide open. That's the moment I can confidently confirm that the machine is listening. [Read more ..](hello-world)

<div style="margin-top:3rem"></div>