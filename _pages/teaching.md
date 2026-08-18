---
layout: page
permalink: /teaching/
title: teaching
description: teaching for ideas is like replication for organisms.
nav: true
nav_order: 7
---
<style>
  .teaching-courses {
    display: grid;
    gap: 1rem;
  }

  .teaching-course {
    padding: 1.1rem 1.2rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 0.65rem;
    background: var(--global-card-bg-color);
  }

  .teaching-course h2 {
    margin: 0 0 0.25rem;
    font-size: 1.2rem;
  }

  .teaching-course > p {
    margin: 0 0 0.9rem;
    color: var(--global-text-color-light);
  }

  .course-year {
    display: grid;
    grid-template-columns: 7rem minmax(0, 1fr);
    gap: 0.9rem;
    padding: 0.75rem 0;
    border-top: 1px solid var(--global-divider-color);
  }

  .course-year:last-child {
    padding-bottom: 0;
  }

  .course-term {
    font-weight: 650;
  }

  .course-year p {
    margin: 0;
  }

  .course-link {
    display: inline-block;
    margin-top: 0.25rem;
  }

  .earlier-teaching {
    margin-top: 2.4rem;
  }

  .earlier-teaching h2 {
    margin-bottom: 1rem;
  }

  .earlier-year {
    display: grid;
    grid-template-columns: 4rem minmax(0, 1fr);
    gap: 1rem;
    padding: 0.85rem 0;
    border-top: 1px solid var(--global-divider-color);
  }

  .earlier-year:last-child {
    border-bottom: 1px solid var(--global-divider-color);
  }

  .earlier-year h3,
  .earlier-year p {
    margin: 0;
  }

  .earlier-year h3 {
    font-size: 1rem;
  }

  .earlier-year p + p {
    margin-top: 0.7rem;
  }

  @media (max-width: 540px) {
    .course-year,
    .earlier-year {
      grid-template-columns: 1fr;
      gap: 0.25rem;
    }
  }
</style>

<div class="teaching-courses">
  <section class="teaching-course">
    <h2>CST 5020 · Convex Optimization</h2>
    <p>Westlake University, Hangzhou</p>

    <div class="course-year">
      <div class="course-term">Spring 2026</div>
      <div>
        <p>Convex Optimization</p>
        <a class="course-link" href="{{ '/cvxopt/' | relative_url }}">Syllabus, schedule, and course materials →</a>
      </div>
    </div>

    <div class="course-year">
      <div class="course-term">Spring 2025</div>
      <div>
        <p>Optimization and Applications</p>
        <a class="course-link" href="{{ '/opt_app/' | relative_url }}">Syllabus, lectures, assignments, and schedule →</a>
      </div>
    </div>
  </section>

  <section class="teaching-course">
    <h2>CST 5034 · Control and Computation in Biological Systems</h2>
    <p>Westlake University, Hangzhou</p>

    <div class="course-year">
      <div class="course-term">Fall 2025</div>
      <div>
        <p>Control and Computation in Biological Systems</p>
        <a class="course-link" href="{{ '/ccbs/' | relative_url }}">Syllabus, textbook, videos, assignments, and lecture notes →</a>
      </div>
    </div>
  </section>
</div>

<section class="earlier-teaching">
  <h2>Earlier teaching and mentorship</h2>

  <div class="earlier-year">
    <h3>2022</h3>
    <p>
      <strong>UC San Diego · Phys 176/276</strong><br>
      Guest lecturer for a one-week lecture series on analysis and computation of dynamic metabolism.
      <a href="https://drive.google.com/drive/folders/1F2NKVamFPvReaVWz3b19uSwzoXaECC5Q?usp=sharing">Slides, homework, and solutions →</a>
    </p>
  </div>

  <div class="earlier-year">
    <h3>2021</h3>
    <div>
      <p>
        <strong>Caltech · Bi 23, Section 5</strong><br>
        Instructor, BioTutorials: Analysis and Design of Biological Circuits.
        <a href="https://drive.google.com/drive/folders/1vWiFMJn4BwHijoefonwDXYIkdbjhaf9r?usp=sharing">Video recordings and lecture notes →</a>
      </p>
      <p>
        <strong>Caltech · CMS/CS 155</strong><br>
        Teaching assistant for <a href="https://github.com/lakigigar/Caltech-CS155-2021">Machine Learning and Data Mining</a>, instructed by
        <a href="https://pachterlab.github.io/">Lior Pachter</a>.
      </p>
    </div>
  </div>

  <div class="earlier-year">
    <h3>2018</h3>
    <div>
      <p>
        <strong>Caltech · Summer research</strong><br>
        Mentor for Meichen Fang, an undergraduate researcher in the Doyle group, who later began PhD studies in Caltech Bioengineering.
      </p>
      <p>
        <strong>Caltech · Bi/BE/CS 183</strong><br>
        Teaching assistant for Introduction to Computational Biology and Bioinformatics, instructed by
        <a href="https://pachterlab.github.io/">Lior Pachter</a> and <a href="https://thomsonlab.caltech.edu/">Matt Thomson</a>.
      </p>
    </div>
  </div>

  <div class="earlier-year">
    <h3>2015</h3>
    <p>
      <strong>Washington University in St. Louis · Math 5061</strong><br>
      Teaching assistant for Theory of Statistics, instructed by <a href="https://www.math.wustl.edu/~jmding/">Jimin Ding</a>.
    </p>
  </div>
</section>
