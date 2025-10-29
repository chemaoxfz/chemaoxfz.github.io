---
layout: page
permalink: /ccbs/
title: CST 5034 CCBS
description: Course materials for CST 5034 - Control and Computation in Biological Systems, Fall 2025
img: assets/img/12.jpg
nav: true
nav_order: 10
---

**Course name:** CST 5034 - Control and Computation in Biological Systems, Fall 2025
[Syllabus](https://chemaoxfz.github.io/assets/ccbs/2025fall/syllabus.pdf)
<!-- [Textbook](https://www.amazon.com/Introduction-Systems-Biology-Mathematical-Computational/dp/1439837171) -->

**Time:** Thursdays 9:50a.m. - 12:15p.m.

**Location:** E10-306 on Yungu campus

**Website:** [https://chemaoxfz.github.io/ccbs](https://chemaoxfz.github.io/ccbs)

**Lecturer:** Fangzhou Xiao
**Office hour and location:** 1 hour/week, by email appointment, E1-321

**TAs:** Yihang Ding; Qinguo Liu

**TA Office hours:** 1 hour/week, 10am (Yihang), 2pm (Qinguo) per Tuesday, at E3-111 BMAC lab 2nd floor

**Lecture scribe template:** [latex template](https://www.overleaf.com/read/fjbfzgqnswjz#af1340)

### Course Description

Biological organisms exhibit many fascinating behaviors, from magical transformation of matter via thousands of steps of metabolic reactions, to robust homeostasis adapting to rapidly shifting environments, to survival and growth that balances persistence in extreme conditions and all-out ventures into opportunistic moments of rich nutrients, to dominance and terraforming of surroundings to its own advantage. Such complex behaviors involving lots of interacting components demand a rigorous and quantitative way of reasoning, like how we reason about complex engineered machines. In this course, we introduce and master tools of reasoning from three different schools of thought pondering about life: physics, system, and industry. Physics asks what life is as an object. System asks how life works as a machine. Industry asks how life could be useful as a tool. These three schools of thought have distinct origins, approaches to analysis, and goals. They shape how we think about life forms. The tools we learn from them span a wide range, from order of magnitude estimate to design of a single protein molecule, from Markov chains to control systems, from simple reasoning based on central dogma to whole-genome models. By the end of the course, you will be able to integrate these tools and perspectives into a cohesive whole and have the confidence to reason about any biological problem thrown at you, from single molecules to populations of organisms. No background needed, but an exuberant love for biology is mandatory.

### Learning Objectives
- To understand and master the tools of analysis in quantitative synthetic biology
- To formulate problems encountered in synthetic biology into forms analyzable using the tools in quantitative synthetic biology
- To get familiar with the theoretical background and technical aspects underlying the tools

### Course Video
- [Video records](https://pan.westlake.edu.cn:443/link/BE96441505CC9ACFEF78FFA268FCBA47)；Passport: hWut
- Lecture video recordings will be updated weekly

<br>

### Schedule

| Number | Date       | Topic          | Reference Materials | Problem Sets | Lecture Notes
| --    | :---       | :----------------- |:-------------| ----- | ----- |
|  1     | 20250904   | Order of Magnitude (OoM) reasoning in physics and biology  | [cell biology by the numbers](https://book.bionumbers.org/); [physical biology of the cell](https://www.rpgroup.caltech.edu/aph161/2022/index.html) | [pset1](https://chemaoxfz.github.io/assets/ccbs/2025fall/lecture1/2025FL_CCBS_hw01.pdf)| [written note](https://chemaoxfz.github.io/assets/ccbs/2025fall/lecture1/202509-CCBS-lecture-notes-01-OoM.pdf); [scribe note](https://chemaoxfz.github.io/assets/ccbs/2025fall/lecture1/2025FL_CCBS_scribe_lecture1.pdf);([source code](https://www.overleaf.com/read/fbnqbwbwmwtr#bd4ee8)) |
|  2     | 20250911  | Chemical reaction networks (CRNs), elementary vs composite reactions, estimate of reaction rate, law of mass action, rate equations| (material) | [pset2](https://chemaoxfz.github.io/assets/ccbs/2025fall/lecture2/2025FL_CCBS_hw02.pdf) | [written note](https://chemaoxfz.github.io/assets/ccbs/2025fall/lecture2/202509-CCBS-lecture-notes-02-CRN_202509092201_32013.pdf);(scribe note) |
|  3     | 20250918   | Analysis of 1D and 2D dynamical systems, phase portrait, local stability, polynomial dynamics of CRNs, diversity of bioregulation by time scale separation |Chapter 1 to 8 of Strogatz book is a good reference on phase portraits; CRNs the mathematical formulation is presented in Feinberg book  (see references below) | (same hw as week 2) |[written note](https://chemaoxfz.github.io/assets/ccbs/2025fall/lecture3/202509-CCBS-lecture-notes-03-bioregulation_202509181251_21385.pdf); [scribe note](https://chemaoxfz.github.io/assets/ccbs/2025fall/lecture3/2025FL_CCBS_scribe_lecture03_v3.pdf); ([source code](https://chemaoxfz.github.io/assets/ccbs/2025fall/lecture3/2025FL_CCBS_scribe_lecture03_v3.zip)) |
|  4     | 20250925  | Adaptation biomachines. Conceptual basics of control. Adaptation as integral control. How biology implements integral control differently from electrical circuits. IFFL works in biology but not in traditional engineering.  | A good intro to control is [the book by Astrom and Murray]((https://www.cds.caltech.edu/~murray/FBS/Second_Edition.html)), adaptation in systems biology is discussed in some chapters of [Alon's book](https://www.amazon.com/Introduction-Systems-Biology-Mathematical-Computational/dp/1439837171) and in Chapter 2 to 6 of this [website](biocircuits.github.io) | [pset3](https://chemaoxfz.github.io/assets/ccbs/2025fall/lecture4/2025FL_CCBS_hw03.pdf) | [written note](https://chemaoxfz.github.io/assets/ccbs/2025fall/lecture4/202509-CCBS-lecture-notes-04-diverse-bioregulation-and-adaptation-biomachine.pdf);[scribe note](https://chemaoxfz.github.io/assets/ccbs/2025fall/lecture4/Note_Lecture4.pdf)([source code](https://chemaoxfz.github.io/assets/ccbs/2025fall/lecture4/Note_Lecture4.zip)) |
|        |  20251002          | holiday |
|  5     |  20251009 | Stochasticity, chemical master equation | (material)  | [pset4](https://chemaoxfz.github.io/assets/ccbs/2025fall/lecture5/2025FL_CCBS_hw04.pdf) |[written note](https://chemaoxfz.github.io/assets/ccbs/2025fall/lecture5/202509-CCBS-lecture-notes-05-adaptation-biomachine_202510090338_05347.pdf)(scribe note) |
|  6     | 20251016  | noise analysis, Gillespie algorithm, gene expression burstyness, bimodal distribution, ergodicity.  | (material) | [pset5](https://chemaoxfz.github.io/assets/ccbs/2025fall/lecture6/2025FL_CCBS_hw05.pdf) | [written note](https://chemaoxfz.github.io/assets/ccbs/2025fall/lecture6/202509-CCBS-lecture-notes-06-noise-and-energy-equi_202510161018_41883.pdf)(scribe note) |
|  7     |  20251023  | Energy and equilibrium statistical mechanics applied to transcriptional and enzymatic regulation, markov chain.  | (material) | (same hw as last week) | [written note](https://chemaoxfz.github.io/assets/ccbs/2025fall/lecture7/202509-CCBS-lecture-notes-07-energy-equilibrium-re_202510251507_57260.pdf) |
|  8     |  20251030  | Computation biomachines. Biological networks as calculators, computers, artificial neural networks, and ... themselves? | (material) | (hw) | (notes) |
|  9     |  20251106  | PROTEIN DESIGN! HANDS ON!!!! Nupack, Rosetta, Fold it. |(material) | (hw) | (notes) |
|  10    |  20251113  | Combinatorial regulation and promiscuous interactions in cell signaling and cell fate decisions, also ultrasensitivity in ligand-receptor binding. ROP as a way for holistic analysis, three archetypal behaviors in a binding reaction. Holistic analysis solving the above problems. Behavior in ROP as trajectory through regimes. Computation of binding-catalysis networks - homotopy continuation.   | (material) | (hw) | (notes) |
|  11    | 20251120   |  (1) Flux balance analysis (metabolic engineering), bioenergetics and metabolism (where does energy of ATP come from), (2) Growth dynamics, proteome partition, diauxie, upshift/downshift  | (material) | (hw) | (notes) |

<br>

### Reference

This course does not have a textbook and all materials are self-contained. But the following reference might be helpful depending on your particular interests.

[Biomolecular Feedback Systems](http://www.cds.caltech.edu/~murray/BFSwiki/index.php/Main_Page) by Richard Murray. A nice (and free!) reference for general background on modeling of biological circuits (most relevant are the first 3 chapters), time-scale separation by singular perturbation, stochasticity, and some on feedback and control.

[Feedback Systems](https://www.cds.caltech.edu/~murray/FBS/Second_Edition.html) by Karl J. Åström and Richard M. Murray. A great introduction to control systems, freely available online. This book is especially good on giving an intuitive yet rigorous picture of the ideas of control theory.

[An Introduction to Systems Biology](https://www.amazon.com/Introduction-Systems-Biology-Mathematical-Computational/dp/1439837171) by Uri Alon. Another good general reference on the interplay between systems thinking based on simple models and biological implications.

[biocircuits.github.io](https://biocircuits.github.io/). A very good course with abundant online materials! With lots of recent examples, papers, and ready-to-use code implementing analysis and simulations of many biocircuits.

[Cell biology by the numbers](https://book.bionumbers.org). A book freely available in easily accessible webpage form! Lots of interesting vignettes for Order of Magnitude (OoM) reasoning about biology. For example, do you know an mRNA molecule is about 10 times larger (volume or mass) than the protein it encodes?

[Nonlinear dynamical systems and Chaos](https://www.amazon.com/Nonlinear-Dynamics-Chaos-Third-Applications/dp/0367261979)  by Steven Strogatz. An accessible book, especially good at giving intuitive descriptions of dynamics for 1D and 2D systems.

[Foundations of Chemical Reaction Network Theory](https://link.springer.com/book/10.1007/978-3-030-03858-8) by Martin Feinberg. A book on the more mathematical aspects of chemical reaction networks, especially equilibrium dynamics. A good reference book. Caution: try not to lose sight of biology, then you won't be daunted by the math wrappings.


