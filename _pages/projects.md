---
layout: page
title: research
permalink: /projects/
description: Ongoing, future and past research threads with accessible introductions.
nav: true
nav_order: 3
display_categories: [ongoing, past]
---
<!-- pages/projects.md -->
<style>
  .research-index {
    margin-top: 2rem;
  }

  .research-index__section + .research-index__section {
    margin-top: 3rem;
  }

  .research-index__heading {
    margin: 0;
    padding-bottom: 0.65rem;
    border-bottom: 1px solid var(--global-divider-color);
    font-size: 1.45rem;
    text-transform: capitalize;
  }

  .research-index__list {
    padding: 0;
    margin: 0;
    list-style: none;
  }

  .research-project {
    display: grid;
    grid-template-columns: minmax(10.5rem, 13.5rem) minmax(0, 1fr);
    gap: 1.5rem;
    align-items: center;
    padding: 1.5rem 0;
    border-bottom: 1px solid var(--global-divider-color);
  }

  .research-project--text-only {
    grid-template-columns: minmax(0, 1fr);
  }

  .research-project__media {
    display: block;
    overflow: hidden;
    border: 1px solid var(--global-divider-color);
    border-radius: 0.5rem;
    background: var(--global-card-bg-color);
  }

  .research-project__media:focus-visible,
  .research-project__title a:focus-visible,
  .research-project__link:focus-visible {
    border-radius: 0.2rem;
    outline: 3px solid var(--global-theme-color);
    outline-offset: 3px;
  }

  .research-project__media figure,
  .research-project__media picture {
    display: block;
    margin: 0;
  }

  .research-project__media img {
    display: block;
    width: 100%;
    height: 8.75rem;
    padding: 0.4rem;
    object-fit: contain;
    transition: transform 180ms ease;
  }

  .research-project__media:hover img {
    transform: scale(1.025);
  }

  .research-project__title {
    margin: 0 0 0.45rem;
    font-size: 1.25rem;
    line-height: 1.35;
  }

  .research-project__title a {
    color: var(--global-text-color);
  }

  .research-project__title a:hover {
    color: var(--global-theme-color);
    text-decoration: none;
  }

  .research-project__description {
    max-width: 50rem;
    margin: 0 0 0.75rem;
    line-height: 1.6;
  }

  .research-project__link {
    display: inline-block;
    font-weight: 500;
  }

  @media (max-width: 575.98px) {
    .research-project {
      grid-template-columns: minmax(0, 1fr);
      gap: 1rem;
      padding: 1.25rem 0;
    }

    .research-project__media {
      width: min(100%, 22rem);
    }

    .research-project__media img {
      height: auto;
      max-height: 13rem;
      aspect-ratio: 16 / 10;
    }
  }

  @media (prefers-reduced-motion: reduce) {
    .research-project__media img {
      transition: none;
    }
  }

  .research-index__heading.research-ai__heading {
    text-transform: none;
  }

  .research-ai__lead {
    max-width: 50rem;
    margin: 1.25rem 0 0.25rem;
    line-height: 1.6;
  }

  .research-ai__tag {
    display: block;
    margin-bottom: 0.3rem;
    color: var(--global-theme-color);
    font-size: 0.75rem;
    font-weight: 600;
    letter-spacing: 0.08em;
    text-transform: uppercase;
  }

  .research-ai__commandments {
    max-width: 50rem;
    margin: 0 0 0.75rem;
    padding-left: 2.25rem;
    list-style: upper-roman;
  }

  .research-ai__commandments li {
    margin: 0.35rem 0;
    padding-left: 0.25rem;
    line-height: 1.55;
  }

  .research-ai__commandments li::marker {
    color: var(--global-theme-color);
    font-weight: 600;
  }

  .research-ai__pcaps {
    display: grid;
    grid-template-columns: max-content minmax(0, 1fr);
    gap: 0.3rem 1rem;
    max-width: 50rem;
    margin: 0 0 0.75rem;
  }

  .research-ai__pcaps dt,
  .research-ai__pcaps dd {
    margin: 0;
  }

  .research-ai__pcaps dt {
    font-weight: 600;
  }

  .research-ai__pcaps dt::first-letter {
    color: var(--global-theme-color);
  }

  .research-ai__links {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4rem 1.5rem;
  }
</style>

<div class="research-index">
  {% if site.enable_project_categories and page.display_categories %}
    {% for category in page.display_categories %}
      {% assign categorized_projects = site.projects | where: 'category', category %}
      {% assign sorted_projects = categorized_projects | sort: 'importance' %}
      {% if sorted_projects.size > 0 %}
        <section class="research-index__section" aria-labelledby="{{ category | slugify }}">
          <h2 class="research-index__heading" id="{{ category | slugify }}">{{ category }}</h2>
          <ul class="research-index__list" role="list">
            {% for project in sorted_projects %}
              {% if project.redirect %}
                {% assign project_href = project.redirect %}
              {% else %}
                {% assign project_href = project.url | relative_url %}
              {% endif %}
              {% capture project_title_id %}research-project-{{ category | slugify }}-{{ forloop.index }}{% endcapture %}
              {% capture project_alt %}Illustration for {{ project.title }}{% endcapture %}
              <li>
                <article class="research-project{% unless project.img %} research-project--text-only{% endunless %}">
                  {% if project.img %}
                    <a class="research-project__media" href="{{ project_href }}" aria-labelledby="{{ project_title_id | strip }}">
                      {% include figure.liquid path=project.img sizes="(min-width: 576px) 216px, 90vw" alt=project_alt %}
                    </a>
                  {% endif %}
                  <div class="research-project__content">
                    <h3 class="research-project__title" id="{{ project_title_id | strip }}">
                      <a href="{{ project_href }}">{{ project.title }}</a>
                    </h3>
                    <p class="research-project__description">{{ project.description }}</p>
                    <a class="research-project__link" href="{{ project_href }}" aria-label="Read about {{ project.title | escape }}">
                      Explore this research <span aria-hidden="true">&rarr;</span>
                    </a>
                  </div>
                </article>
              </li>
            {% endfor %}
          </ul>
        </section>
      {% endif %}
    {% endfor %}
  {% else %}
    {% assign sorted_projects = site.projects | sort: 'importance' %}
    <section class="research-index__section" aria-labelledby="research-category-all">
      <h2 class="research-index__heading" id="research-category-all">Research projects</h2>
      <ul class="research-index__list" role="list">
        {% for project in sorted_projects %}
          {% if project.redirect %}
            {% assign project_href = project.redirect %}
          {% else %}
            {% assign project_href = project.url | relative_url %}
          {% endif %}
          {% capture project_title_id %}research-project-{{ forloop.index }}{% endcapture %}
          {% capture project_alt %}Illustration for {{ project.title }}{% endcapture %}
          <li>
            <article class="research-project{% unless project.img %} research-project--text-only{% endunless %}">
              {% if project.img %}
                <a class="research-project__media" href="{{ project_href }}" aria-labelledby="{{ project_title_id | strip }}">
                  {% include figure.liquid path=project.img sizes="(min-width: 576px) 216px, 90vw" alt=project_alt %}
                </a>
              {% endif %}
              <div class="research-project__content">
                <h3 class="research-project__title" id="{{ project_title_id | strip }}">
                  <a href="{{ project_href }}">{{ project.title }}</a>
                </h3>
                <p class="research-project__description">{{ project.description }}</p>
                <a class="research-project__link" href="{{ project_href }}" aria-label="Read about {{ project.title | escape }}">
                  Explore this research <span aria-hidden="true">&rarr;</span>
                </a>
              </div>
            </article>
          </li>
        {% endfor %}
      </ul>
    </section>
  {% endif %}
  <section class="research-index__section" aria-labelledby="research-with-ai">
    <h2 class="research-index__heading research-ai__heading" id="research-with-ai">Research with AI</h2>
    <p class="research-ai__lead">
      An agent output is not research.
      It becomes research when a human can understand it, defend it and communicate it.
      That rule shapes how I do research with AI agents.
      Below are the commandments I work by, the scaffold I use to tell an agent what I want, the camp I organized, where I taught both, and two open skills that turn the practice into procedures an agent can follow.
    </p>
    <ul class="research-index__list" role="list">
      <li>
        <article class="research-project research-project--text-only">
          <div class="research-project__content">
            <span class="research-ai__tag">Stance</span>
            <h3 class="research-project__title">
              <a href="https://pebble-biofusion.github.io/workshop/method/">Commandments of Research-with-AI</a>
            </h3>
            <p class="research-project__description">Four rules fix how a researcher stands relative to an AI agent.</p>
            <ol class="research-ai__commandments">
              <li><b>AI is our minion, not our peer.</b> Own every claim, or do not use it. If you cannot explain it, it is vapor.</li>
              <li><b>AI is a cyber-arm.</b> Attach it to the work you care about most, not the chores you dislike.</li>
              <li><b>Your input&ndash;output bandwidth is the bottleneck.</b> Not the model's power. Specification in, comprehension out.</li>
              <li><b>Be above AI on everything you think about.</b> Generic AI output is the floor, not the ceiling.</li>
            </ol>
            <a class="research-project__link" href="https://pebble-biofusion.github.io/workshop/method/">The method we taught at PEBBLE BioFusion <span aria-hidden="true">&rarr;</span></a>
          </div>
        </article>
      </li>
      <li>
        <article class="research-project research-project--text-only">
          <div class="research-project__content">
            <span class="research-ai__tag">Scaffold</span>
            <h3 class="research-project__title">
              <a href="https://pebble-biofusion.github.io/workshop/materials/202607-PEBBLE-PCAPS-seed.pdf">PCAPS</a>
            </h3>
            <p class="research-project__description">
              A specification an agent can act on has the same shape as a scientific story worth hearing.
              PCAPS is that shape, five links in one chain of logic.
            </p>
            <dl class="research-ai__pcaps">
              <dt>Problem</dt><dd>What are you tackling?</dd>
              <dt>Challenge</dt><dd>Why is it not solved yet?</dd>
              <dt>Approach</dt><dd>What is your take, and why?</dd>
              <dt>Proof</dt><dd>What evidence shows it works?</dd>
              <dt>Significance</dt><dd>What is the contribution, and who cares?</dd>
            </dl>
            <a class="research-project__link" href="https://pebble-biofusion.github.io/workshop/materials/202607-PEBBLE-PCAPS-seed.pdf">The PCAPS slides (PDF) <span aria-hidden="true">&rarr;</span></a>
          </div>
        </article>
      </li>
      <li>
        <article class="research-project research-project--text-only">
          <div class="research-project__content">
            <span class="research-ai__tag">Teaching</span>
            <h3 class="research-project__title">
              <a href="https://pebble-biofusion.github.io/">PEBBLE BioFusion 2026, an AI-native research camp</a>
            </h3>
            <p class="research-project__description">
              I organized PEBBLE BioFusion 2026, a summer research camp designed from the ground up for the age of AI.
              Westlake University's Center for Interdisciplinary Studies hosted and funded it.
              AI now supplies tutorials, literature search, code and first drafts on demand.
              So the camp trained what AI does not reliably supply: taste in choosing questions, rigor in building a chain of logic, and the courage to pursue a bold question all the way through.
              Week one opened five live questions, and week two handed the hours to the students.
              In eleven days, forty-five students wrote sixteen manuscripts.
            </p>
            <a class="research-project__link" href="https://pebble-biofusion.github.io/">Schedule, tutorials and student work <span aria-hidden="true">&rarr;</span></a>
          </div>
        </article>
      </li>
      <li>
        <article class="research-project research-project--text-only">
          <div class="research-project__content">
            <span class="research-ai__tag">Open skill</span>
            <h3 class="research-project__title">
              <a href="https://github.com/chemaoxfz/orchestrated-research">orchestrated-research</a>
            </h3>
            <p class="research-project__description">
              This skill makes an agent the orchestrator of a long research project, which it runs in stages with dedicated agents.
              Two dedicated writers keep their own memory across sessions.
              One writes a tutorial like the main text of a high-impact paper, and the other a technical companion that holds every derivation, proof and computation.
              I distilled it from two of my own long projects, and it works in Claude Code, Codex and other agents that read skills.
            </p>
            <a class="research-project__link" href="https://github.com/chemaoxfz/orchestrated-research">View on GitHub <span aria-hidden="true">&rarr;</span></a>
          </div>
        </article>
      </li>
      <li>
        <article class="research-project research-project--text-only">
          <div class="research-project__content">
            <span class="research-ai__tag">Open skill</span>
            <h3 class="research-project__title">
              <a href="https://github.com/chemaoxfz/idea-to-essay">idea-to-essay</a>
            </h3>
            <p class="research-project__description">
              This skill develops one research idea into a standalone HTML essay grounded in the literature.
              It digests the idea into a thesis you could argue with, downloads and verifies the full texts it cites, computes every number and figure from code, and only then writes.
              I write the essays on this site with it.
            </p>
            <div class="research-ai__links">
              <a class="research-project__link" href="https://github.com/chemaoxfz/idea-to-essay">View on GitHub <span aria-hidden="true">&rarr;</span></a>
              <a class="research-project__link" href="{{ '/essays/' | relative_url }}">Read the essays <span aria-hidden="true">&rarr;</span></a>
            </div>
          </div>
        </article>
      </li>
    </ul>
  </section>
</div>
