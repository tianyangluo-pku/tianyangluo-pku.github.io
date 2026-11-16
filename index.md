---
layout: homepage
title: About
seo_title: Tianyang Luo | Peking University
---

<div class="about-heading">
  <h1 id="tianyang-luo">{{ site.title }} <span class="name-chinese">&#65288;&#20013;&#25991;&#21517;&#65289;</span></h1>
</div>

## About

<div class="about-intro" markdown="1">

{% if site.avatar and site.avatar != "" %}
<figure class="about-portrait">
  <img src="{{ site.avatar | relative_url }}" alt="Portrait of Tianyang Luo" width="480" height="640" />
</figure>
{% endif %}

I am a Ph.D. student at the **School of Integrated Circuits, Peking University**, advised by **Prof. Yimao Cai**. My research explores **emerging memory technologies** and **memory-centric computing architectures** for efficient LLM inference.

</div>

### Research Interests

- Emerging Memory Technologies
- In-Memory and Near-Memory Computing Architectures
- Memory-Centric AI Acceleration

## Experience

### Education

- **Ph.D. Student**, School of Integrated Circuits, Peking University, 2025&ndash;present
- **B.S. in Applied Physics**, School of Electronics Engineering and Computer Science, Peking University, 2021&ndash;2025
- **B.Econ. in Economics**, National School of Development, Peking University, 2022&ndash;2025

{% include publications.md homepage=true hide_controls=true %}
