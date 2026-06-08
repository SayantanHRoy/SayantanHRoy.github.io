---
permalink: /
excerpt: "Economics PhD candidate at Purdue — structural macro, causal inference, and a data-science background in large-scale ML."
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
         alt="Sayantan Roy." />
  </div>
  <div class="rd-hero__text">
    <h1 class="rd-hero__name">Sayantan Roy</h1>
    <p class="rd-hero__lede">Economics PhD candidate at Purdue, pairing structural macro and causal inference with a data-science background in large-scale ML.</p>
  </div>
</div>

<div class="rd-about" markdown="1">
I am an Economics PhD candidate at Purdue working on spatial macroeconomics: how aggregate shocks, from fiscal stimulus to tariffs, play out unevenly across regions. My job market paper shows that the employment return to stimulus depends on where it is spent, not just how much; a related project builds a multi-region input-output model of how tariffs propagate across sectors and places. Both pair empirical evidence with structural models I solve computationally. Before the PhD, I built production credit-risk models at American Express. I work mostly in Python and JAX.
</div>

<ul class="rd-linkrow">
  <li><a href="https://github.com/SayantanHRoy/CV/blob/main/CV_updated_SayantanRoy.pdf">CV</a></li>
  <!-- TODO: replace with the 1-page résumé PDF link when ready -->
  <li><a href="{{ '/cv/' | relative_url }}">Résumé</a></li>
  <li><a href="https://github.com/SayantanHRoy">GitHub</a></li>
  <li><a href="https://www.linkedin.com/in/sayantan-roy">LinkedIn</a></li>
  <li><a href="mailto:roy175@purdue.edu">Email</a></li>
</ul>

<hr class="rd-divider" />

<div class="rd-cols">

  <section class="rd-col">
    <h2 class="rd-subhead">Selected research</h2>
    <span class="rd-eyebrow">Job market paper</span>
    <p class="rd-paper-title">County Population Size and the Employment Effects of Fiscal Policy</p>
    <p class="rd-finding">Stimulus creates the most jobs in mid-sized counties — local employment responses trace an inverted-U in county population size.</p>
    <ul class="rd-reslinks">
      <!-- TODO: add PDF · Slides · Code links once the draft is public -->
      <li><span class="rd-reslinks__state">Draft coming soon</span></li>
      <li><a href="{{ '/research/' | relative_url }}">More research →</a></li>
    </ul>
  </section>

  <section class="rd-col">
    <h2 class="rd-subhead">Selected projects</h2>

    <p class="rd-project__title">DSGE perturbation solver (Julia → Python)</p>
    <p class="rd-project__desc">SGU/Klein perturbation with SymPy + JAX backends, validated on a two-country IRBC model.</p>
    <ul class="rd-tags">
      <li class="rd-pill">Julia</li>
      <li class="rd-pill">Python</li>
      <li class="rd-pill">JAX</li>
      <li class="rd-pill">SymPy</li>
    </ul>

    <p class="rd-project__title" style="margin-top:1.25rem;">Regional dynamic IO tariff model</p>
    <p class="rd-project__desc">JAX Newton–Krylov steady-state solver at 48×41 scale. <span class="rd-reslinks__state">(in development)</span></p>
    <ul class="rd-tags">
      <li class="rd-pill">JAX</li>
      <li class="rd-pill">Newton–Krylov</li>
    </ul>

    <ul class="rd-reslinks" style="margin-top:1rem;">
      <li><a href="{{ '/projects/' | relative_url }}">All projects →</a></li>
    </ul>
  </section>

</div>
