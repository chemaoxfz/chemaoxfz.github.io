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
</div>
