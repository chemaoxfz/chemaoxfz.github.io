---
layout: page
permalink: /essays/
title: essays
description: Long-form writeups that put an idea in conversation with the literature it belongs to.
nav: true
nav_order: 4
---

<p class="lead">These are research essays: extended, tutorial-like writeups that take one idea, situate it in the
literature it belongs to, and carry it far enough to be worth disagreeing with.</p>

<p>Each is a single self-contained page. Read it start to finish and you should learn the field around
the idea, not just the idea. Figures are drawn to be read. Sources are cited in full, and every claim
that carries weight rests on a paper whose full text was actually read.</p>

<h2>How these are written</h2>

<p>I write them with an agent, following a fixed procedure I have packaged as an open skill:
<a href="https://github.com/chemaoxfz/idea-to-essay" rel="noopener">idea-to-essay</a>. Given an idea, it
digests it into a thesis you could argue with, sweeps the literature and downloads verified full texts,
produces the numbers and figures from code, and only then writes.</p>

<p>Three rules do most of the work. Nothing is cited from an abstract or from memory, so a claim either
has a full text behind it or it is flagged as new. Corrections count as output, so when a paper overturns
something I believed, that goes in the writeup rather than quietly out of it. And every number traces to
a script that runs. The procedure, the tooling and the house style are all in the repository, under MIT,
if you want to run it yourself.</p>

<h2>The essays</h2>

<div class="card mb-3">
  <div class="card-body">
    <h3 class="h5 card-title"><a href="/essays/synbio-history/">Three Schools, Three Shocks</a></h3>
    <p class="text-muted mb-2">A history of synthetic biology, and why its third wave stalled</p>
    <p>Physics, system, and industry have each asked their own question of life. Three times a discovery
    let all three ask it at once. The third time stalled, and the reason is a missing model class.
    Twenty-five sections, nine figures, 111 sources read in full.</p>
  </div>
</div>

<div class="card mb-3">
  <div class="card-body">
    <h3 class="h5 card-title"><a href="/essays/biomachine-tutorial/">The Biomachine Perspective</a></h3>
    <p class="text-muted mb-2">A tutorial on reading cells as machines, and what that buys you</p>
    <p>A cell is a machine. Fix the function, compare the implementations, and let the difference in
    physical constraints explain the difference in architecture. Twenty-one sections, ten figures, worked
    examples, and an interactive demo. This is the perspective the lab is built on.</p>
  </div>
</div>

<div class="card mb-3">
  <div class="card-body">
    <h3 class="h5 card-title"><a href="/essays/structure-and-parameters/">Structure is Sparsity</a></h3>
    <p class="text-muted mb-2">What is actually obtainable about a cell, from what kind of data</p>
    <p>A biochemical model's structure is the support of its parameter vector, so the line between
    structure and parameters is a threshold rather than a kind. Bailey's 2001 split into qualitative
    and quantitative information does not survive putting binding into the network, and Bailey had
    already built the machine that treats them as one. Twenty-eight sections, seven figures, 90
    sources read in full.</p>
  </div>
</div>

<div class="card mb-3">
  <div class="card-body">
    <h3 class="h5 card-title"><a href="/essays/reaction-order/">The Order of a Reaction</a></h3>
    <p class="text-muted mb-2">One log-log slope, five names, and the assumption underneath twenty-five years of argument</p>
    <p>The derivative &part;log&thinsp;v/&part;log&thinsp;x was a measurement before it was a theory. van 't Hoff wrote it
    as a formula in 1884 and called it the number of molecules taking part; Ostwald renamed it "order"
    three years later to say it was not. It arrives again as the Hill coefficient, the reflection
    coefficient, the kinetic order and the elasticity, and two schools of theoretical biochemistry then
    spent twenty-five years disputing whether one was a special case of the other. That dispute is
    reconstructed here from both sides' papers, and resolved: separating binding from catalysis makes
    metabolic control analysis's one assumption exactly true at the layer where it belongs, and a
    computable polytope at the layer where it does not. Twenty-seven sections, fourteen figures, seven
    of them page images of the original sources, 41 sources read in full.</p>
  </div>
</div>

<p class="text-muted"><small>Each essay links into a local <code>literature/</code> archive of full-text
PDFs. That archive is not redistributed here, so those links are inert on the web. Every citation is
complete enough to find the source.</small></p>
