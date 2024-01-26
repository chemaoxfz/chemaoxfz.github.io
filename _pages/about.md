---
layout: about
title: about
permalink: /
subtitle: <a href='#'> Westlake University, School of Engineering </a>. xiaofangzhou@westlake.edu.cn

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>Room E1-321, Yungu Campus</p>
    <p>600 Dunyu Road, Xihu District</p>
    <p>Hangzhou CHINA</p>

news: false # includes a list of news items
latest_posts: false # includes a list of the newest posts
selected_papers: true # includes a list of papers marked as "selected={true}"
social: false # includes social icons at the bottom of the page
---

I'm Fang, an assistant professor in the School of Engineering at Westlake University in Hangzhou China, starting the biomachine architecture and control (BMAC) lab. 
Before this, I was a postdoctoral researcher at [Suckjoon Jun](https://jun.ucsd.edu/) group at UCSD to apply my theoretical framework in engineering to fundamental laws of bacterial survival and growth in dynamic environments. I obtained my PhD in bioengineering at Caltech in 2022, mentored by [John C Doyle](http://www.cds.caltech.edu/~doyle/wiki/index.php?title=Main_Page), and built a theoretical foundation for biocontrol in cells from gene circuits, to metabolism and physiology. My PhD thesis "Biocontrol of Biomolecular Systems: Polyhedral Constraints on Binding's Regulation of Catalysis from Biocircuits to Metabolism" is [here](https://thesis.library.caltech.edu/14652/). Here's my [google scholar site](https://scholar.google.com/citations?user=_iWSHHsAAAAJ&hl=en) and my [CV](https://chemaoxfz.github.io/assets/pdf/cv.pdf).

My career goal is to push for the mature engineering of complex biological machines that fully realizes the unique potential of biotechnology.
In order to do so, not only do we need theoretical understanding and reliable manufacturing of biological parts and components, we also need a systems theory to understand how to put parts together and what can and cannot be achieved. Examples from other engineering disciplines are Turing machines for computers, information channel for communication networks, linear input output systems for electrical circuits, and thermodynamics for heat engines.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-0" src="{{ '/assets/img/fig-system-theory-intro.png' | relative_url }}" alt="" title="System theory is important to understand what can be achieved by putting parts together into a machine."/>
    </div>
</div>
<div class="caption">
    Taking other engineering disciplines as motivations, we see system theory is important to understand what can and cannot be achieved by putting parts together into a machine.
</div>

My PhD therefore focused on developing a systems theory tailored to biomolecular systems in cells.
This culminated into the following statements. See the [research](https://chemaoxfz.github.io/projects/) page for details. 
<!-- Some preliminary ideas of this work were generated during my visit to [Mustafa Khammash](https://bsse.ethz.ch/ctsb) group in the summer of 2019, where I had the joy to walk along (and sometimes drift along) [the Rhine river](https://www.basel.com/en/activities-excursions/swimming-rhine). -->

Biomolecular systems are binding and catalysis reactions. Catalysis determines the direction of change, while binding regulates how the catalysis rates vary with reactant concentrations.
The holistic regulatory profile can be captured by the reaction order of catalysis, which in turn is constrained in polyhedra determined by the stoichiometry of binding.
In summary, since cells control catalysis by binding, cells control catalysis rates by regulating reaction orders. 
This also has ramifications in several directions. 
On metabolism, by incorporating the constraint that reaction orders of metabolic fluxes, not the fluxes themselves, are controlled, we can predict metabolism dynamics directly from network stoichiometry, e.g. glycolytic oscillations and growth arrests.
On systems biology, this derives Analysis by Binding and Catalysis (ABC) that allows discovery of necessary and sufficient conditions for a circuit to function, holistic comparisons of different circuit implementations, e.g. activator versus repressor, and enables biocircuit design where we know when a design will work, and when a design will fail.
On dynamics and control of biocircuits, reaction order can work as a robust basis for stability, perfect adaptation, multistability and oscillations. 
Lyapunov functions and dissipativity theory tailored for biomolecular systems can be constructed based on reaction order.
On the mathematics of biology, it relates bioregulation to convex polyhedra, log derivative operator decompositions, and fundamental rules of calculus for positive variables.

The two figures below illustrate the system view that this promotes. For more details see the [research](https://chemaoxfz.github.io/projects/) page.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-0" src="{{ '/assets/img/fig-enzymatic-reaction-polytope-full.png' | relative_url }}" alt="" title="log derivative polyhedron of simple binding"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-0" src="{{ '/assets/img/fig-constraint-based.png' | relative_url }}" alt="" title="flux exponent control (FEC) in constraint-based modelling of metabolism"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-0" src="{{ '/assets/img/fig-math-decomposition-tree-simple.png' | relative_url }}" alt="" title="dominance decomposition tree (DTT) technique based on the mathematics of log derivative operator decomposition"/>
    </div>
</div>
<div class="caption">
    Left, for a simple binding reaction of E and S binds to complex C, the reaction order of C (with log derivative as its continuous analogue) is constrained inside the triangular polyhedron. 
    Middle, flux exponent control (FEC) as a constraint-based modelling of metabolism that can capture metabolism dynamics, utilizing more biological constraints than flux balance analysis. 
    Right, understanding how the holistic regulatory profile of binding reactions relate to the mathematics of log derivative operators' decomposition rules enables a technique for analysis of log derivative polyhedra called dominance decomposition tree (DDT).
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-0" src="{{ '/assets/img/fig-iff-polytope-degradation.gif' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    Example of how log derivative polyhedra can capture the holistic behavior of a biocircuit. This is an incoherent feedforward (IFF) circuit with disturbance intput w activating both x1 and x2, and x2 inhibits x1 by catalyzing x1's degradation. C denotes the reaction complex formed for x1's degradation catalyzed by x2. The upper right triangle is the log derivative polyhedron of C, with the red corner near (1,1) corresponding to the adaptation regime where x1 is robust to disturbance w. When the log derivative deviates away from the red corner, x1 can no longer adapt. We see this fails for disturbance w that is larger than reference.
</div>

