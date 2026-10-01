---
permalink: /
excerpt: "Economics PhD candidate at Purdue: structural macro, causal inference, and a data-science background in large-scale ML."
author_profile: false
redirect_from:
  - /about/
  - /about.html
---

<!-- ================================================================
     HOME — hero + two columns
     DRAFT COPY (from build spec §3). Confirm/rewrite hero + About in
     your own voice before merging. Photo: /images/profile.jpg — swap
     if you have a higher-res source for the duotone treatment.
     ================================================================ -->

<div class="rd-hero">
  <div class="rd-hero__photo rd-photo">
    <img src="{{ '/images/profile.jpg' | relative_url }}"
         alt="Portrait photo of Sayantan Roy." />
  </div>
  <div class="rd-hero__text">
    <h1 class="rd-hero__name">Sayantan Roy</h1>
    <p class="rd-hero__lede">Economics PhD candidate at Purdue.</p>
  </div>
</div>

<div class="rd-about" markdown="1">
I study how aggregate economic shocks play out unevenly across regions. In my [job market paper]({{ '/research/' | relative_url }}#jmp), I examine how the employment effects of fiscal stimulus depend not only on the size of the program, but also on where it is spent. In related work, I study how tariffs propagate across sectors and places with the help of a multi-region input-output model. My research combines empirical evidence with structural models solved computationally. Before the PhD, I built production credit-risk models at American Express. I work mostly in Python and JAX.
</div>

<ul class="rd-linkrow">
  <li><a href="/files/Sayantan-Roy-CV.pdf" target="_blank" rel="noopener">CV</a></li>
  <li><a href="/files/Sayantan-Roy-Resume.pdf" target="_blank" rel="noopener">Résumé</a></li>
  <li><a href="https://github.com/SayantanHRoy">GitHub</a></li>
  <li><a href="https://www.linkedin.com/in/sayantan-roy">LinkedIn</a></li>
  <li><a href="mailto:roy175@purdue.edu">Email</a></li>
</ul>

<hr class="rd-divider" />

<div class="rd-cols">

  <section class="rd-col">
    <h2 class="rd-subhead">Selected research</h2>
    <span class="rd-eyebrow">Job market paper</span>
    <p class="rd-paper-title">Where Does Fiscal Stimulus Create Jobs? Evidence from U.S. Counties</p>
    <p class="rd-finding">Where stimulus is spent matters for how many jobs it creates. Local employment responses to ARRA spending are largest in mid-sized counties and smaller in both small and large ones.</p>
    <ul class="rd-reslinks">
      <!-- TODO: add PDF · Slides · Code links once the draft is public -->
      <li><span class="rd-reslinks__state">Draft coming soon</span></li>
      <li><a href="{{ '/research/' | relative_url }}">More research →</a></li>
    </ul>
  </section>

  <section class="rd-col">
    <h2 class="rd-subhead">Selected projects</h2>

    <p class="rd-project__title">DSGE perturbation solver (Python)</p>
    <p class="rd-project__desc">Built on a SymPy backend, validated on a two-country IRBC model.</p>
    <ul class="rd-tags">
      <li class="rd-pill">Python</li>
      <li class="rd-pill">SymPy</li>
    </ul>

    <p class="rd-project__title" style="margin-top:1.25rem;">Regional dynamic input–output model</p>
    <p class="rd-project__desc">JAX solver. <span class="rd-reslinks__state">(in development)</span></p>
    <ul class="rd-tags">
      <li class="rd-pill">Python</li>
      <li class="rd-pill">JAX</li>
    </ul>

    <ul class="rd-reslinks" style="margin-top:1rem;">
      <li><a href="{{ '/projects/' | relative_url }}">All projects →</a></li>
    </ul>
  </section>

</div>
