---
layout: page
permalink: /people/
title: people
description: members of the BMAC Lab
nav: true
nav_order: 5
---
<style>
  .people-directory {
    --portrait-size: 76px;
  }

  .people-directory h2 {
    margin: 2.25rem 0 1rem;
  }

  .people-directory h2:first-child {
    margin-top: 0;
  }

  .people-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 0.85rem;
  }

  .person-card {
    display: grid;
    grid-template-columns: var(--portrait-size) minmax(0, 1fr);
    gap: 0.9rem;
    align-items: center;
    min-height: calc(var(--portrait-size) + 1.4rem);
    padding: 0.7rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 0.65rem;
    background: var(--global-card-bg-color);
  }

  .person-portrait,
  .person-initials {
    width: var(--portrait-size);
    height: var(--portrait-size);
    border-radius: 50%;
  }

  .person-portrait {
    display: block;
    object-fit: cover;
    object-position: center;
  }

  .person-portrait--right {
    object-position: 68% center;
  }

  .person-portrait--upper {
    object-position: center 35%;
  }

  .person-portrait--lower {
    object-position: center 62%;
  }

  .person-initials {
    display: grid;
    place-items: center;
    border: 1px solid var(--global-divider-color);
    background: var(--global-bg-color);
    color: var(--global-text-color-light);
    font-size: 1rem;
    font-weight: 600;
    letter-spacing: 0.04em;
  }

  .person-name {
    margin: 0 0 0.15rem;
    font-size: 1.05rem;
    font-weight: 650;
    line-height: 1.25;
  }

  .person-role,
  .person-focus,
  .person-contact {
    margin: 0;
    line-height: 1.45;
  }

  .person-role,
  .person-contact {
    font-size: 0.9rem;
  }

  .person-role,
  .person-focus {
    color: var(--global-text-color-light);
  }

  .person-contact {
    margin-top: 0.15rem;
    overflow-wrap: anywhere;
  }

  @media (max-width: 760px) {
    .people-grid {
      grid-template-columns: 1fr;
    }
  }

  @media (max-width: 420px) {
    .people-directory {
      --portrait-size: 64px;
    }

    .person-card {
      gap: 0.75rem;
      padding: 0.6rem;
    }
  }
</style>

<div class="people-directory">
  <h2>Principal investigator</h2>
  <div class="people-grid">
    <article class="person-card">
      <img class="person-portrait" src="{{ '/assets/img/prof_pic.jpg' | relative_url }}" alt="Fangzhou Xiao" width="76" height="76">
      <div>
        <p class="person-name">Fangzhou Xiao</p>
        <p class="person-role">Principal investigator · 2024–present</p>
        <p class="person-contact"><a href="mailto:xiaofangzhou@westlake.edu.cn">xiaofangzhou@westlake.edu.cn</a></p>
      </div>
    </article>
  </div>

  <h2>Staff</h2>
  <div class="people-grid">
    <article class="person-card">
      <img class="person-portrait" src="{{ '/assets/img/prof_qym.jpg' | relative_url }}" alt="Yumeng Qin" width="76" height="76" loading="lazy">
      <div>
        <p class="person-name">Yumeng Qin</p>
        <p class="person-role">Administrative assistant · 2023–present</p>
        <p class="person-contact"><a href="mailto:qinyumeng@westlake.edu.cn">qinyumeng@westlake.edu.cn</a></p>
      </div>
    </article>

    <article class="person-card">
      <div class="person-initials" aria-hidden="true">RZ</div>
      <div>
        <p class="person-name">Ruiting Zhang</p>
        <p class="person-role">Lab manager · 2025–present</p>
        <p class="person-contact"><a href="mailto:zhangruiting@westlake.edu.cn">zhangruiting@westlake.edu.cn</a></p>
      </div>
    </article>
  </div>

  <h2>Students and researchers</h2>
  <div class="people-grid">
    <article class="person-card">
      <img
        class="person-portrait person-portrait--right"
        src="{{ '/assets/img/prof_myp.jpg' | relative_url }}"
        alt="Yiping Ma"
        width="76"
        height="76"
        loading="lazy"
      >
      <div>
        <p class="person-name">Yiping Ma</p>
        <p class="person-role">PhD student · 2024–present</p>
        <p class="person-focus">Microbial decision hypercube</p>
        <p class="person-contact"><a href="mailto:mayiping@westlake.edu.cn">mayiping@westlake.edu.cn</a></p>
      </div>
    </article>

    <article class="person-card">
      <img
        class="person-portrait person-portrait--upper"
        src="{{ '/assets/img/prof_dyh.jpg' | relative_url }}"
        alt="Yihang Ding"
        width="76"
        height="76"
        loading="lazy"
      >
      <div>
        <p class="person-name">Yihang Ding</p>
        <p class="person-role">PhD student · 2024–present</p>
        <p class="person-focus">Complex cellular decisions</p>
        <p class="person-contact"><a href="mailto:dingyihang@westlake.edu.cn">dingyihang@westlake.edu.cn</a></p>
      </div>
    </article>

    <article class="person-card">
      <img
        class="person-portrait person-portrait--upper"
        src="{{ '/assets/img/prof_lqg.jpg' | relative_url }}"
        alt="Qinguo Liu"
        width="76"
        height="76"
        loading="lazy"
      >
      <div>
        <p class="person-name">Qinguo Liu</p>
        <p class="person-role">PhD student · 2024–present</p>
        <p class="person-focus">Realizability index</p>
        <p class="person-contact"><a href="mailto:liuqinguo@westlake.edu.cn">liuqinguo@westlake.edu.cn</a></p>
      </div>
    </article>

    <article class="person-card">
      <img
        class="person-portrait person-portrait--lower"
        src="{{ '/assets/img/prof_ljm.jpg' | relative_url }}"
        alt="Jinman Lei"
        width="76"
        height="76"
        loading="lazy"
      >
      <div>
        <p class="person-name">Jinman Lei</p>
        <p class="person-role">PhD student · 2024–present</p>
        <p class="person-focus">Microbial drama in antibiotic resistance</p>
        <p class="person-contact"><a href="mailto:leijinman@westlake.edu.cn">leijinman@westlake.edu.cn</a></p>
      </div>
    </article>

    <article class="person-card">
      <div class="person-initials" aria-hidden="true">CW</div>
      <div>
        <p class="person-name">Chenxiao Wang</p>
        <p class="person-role">PhD student · 2025–present</p>
        <p class="person-focus">Total control of life</p>
        <p class="person-contact"><a href="mailto:wangchenxiao@westlake.edu.cn">wangchenxiao@westlake.edu.cn</a></p>
      </div>
    </article>

    <article class="person-card">
      <div class="person-initials" aria-hidden="true">XW</div>
      <div>
        <p class="person-name">Xinyu Wang</p>
        <p class="person-role">PhD student · 2025–present</p>
        <p class="person-focus">Data-driven design of bionetworks</p>
        <p class="person-contact"><a href="mailto:wangxinyu@westlake.edu.cn">wangxinyu@westlake.edu.cn</a></p>
      </div>
    </article>

    <article class="person-card">
      <div class="person-initials" aria-hidden="true">WZ</div>
      <div>
        <p class="person-name">Wenqin Zhou</p>
        <p class="person-role">PhD student, jointly with Zibo Chen · 2025–present</p>
        <p class="person-focus">Arbitrary design of cell fate</p>
        <p class="person-contact"><a href="mailto:zhouwenqin@westlake.edu.cn">zhouwenqin@westlake.edu.cn</a></p>
      </div>
    </article>

    <article class="person-card">
      <div class="person-initials" aria-hidden="true">HZ</div>
      <div>
        <p class="person-name">Haobo Zheng</p>
        <p class="person-role">PhD student · 2026–present</p>
        <p class="person-focus">Financial crisis eliminating contamination in fermentation</p>
        <p class="person-contact"><a href="mailto:zhenghaobo@westlake.edu.cn">zhenghaobo@westlake.edu.cn</a></p>
      </div>
    </article>

    <article class="person-card">
      <div class="person-initials" aria-hidden="true">YX</div>
      <div>
        <p class="person-name">Ye Xu</p>
        <p class="person-role">PhD student · 2026–present</p>
        <p class="person-focus">Flux exponent control of microbial dynamics</p>
        <p class="person-contact"><a href="mailto:xuye@westlake.edu.cn">xuye@westlake.edu.cn</a></p>
      </div>
    </article>

    <article class="person-card">
      <div class="person-initials" aria-hidden="true">YJ</div>
      <div>
        <p class="person-name">Yanzhang Jiang</p>
        <p class="person-role">Research assistant · 2025–present</p>
        <p class="person-focus">Design of complex binding networks</p>
        <p class="person-contact"><a href="mailto:jiangyanzhang@westlake.edu.cn">jiangyanzhang@westlake.edu.cn</a></p>
      </div>
    </article>

    <article class="person-card">
      <div class="person-initials" aria-hidden="true">XF</div>
      <div>
        <p class="person-name">Xinwen Fan</p>
        <p class="person-role">Visiting scholar · from August 2026</p>
        <p class="person-focus">Robust synthetic cell platform for bioregulation in growing and dividing systems</p>
      </div>
    </article>

    <article class="person-card">
      <div class="person-initials" aria-hidden="true">JZ</div>
      <div>
        <p class="person-name">Jiarui Zhang</p>
        <p class="person-role">Visiting student · 2025–present</p>
        <p class="person-focus">Monomer repressilator</p>
      </div>
    </article>

    <article class="person-card">
      <div class="person-initials" aria-hidden="true">QW</div>
      <div>
        <p class="person-name">Qianrui (Richard) Wang</p>
        <p class="person-role">Visiting undergraduate student, University of Cambridge · July 2026–present</p>
        <p class="person-focus">
          Extending binding and catalysis networks to include electrical potential; optimal control of neural systems and networks
        </p>
      </div>
    </article>
  </div>

  <h2>Lab alumni</h2>
  <div class="people-grid">
    <article class="person-card">
      <div class="person-initials" aria-hidden="true">YH</div>
      <div>
        <p class="person-name">Yuyang Han</p>
        <p class="person-role">Visiting student · 2025–May 2026</p>
        <p class="person-focus">Retrograde of yeast cell cycle</p>
      </div>
    </article>

    <article class="person-card">
      <img class="person-portrait" src="{{ '/assets/img/prof_fjb.jpg' | relative_url }}" alt="Jinbin Fan" width="76" height="76" loading="lazy">
      <div>
        <p class="person-name">Jinbin Fan</p>
        <p class="person-role">Research assistant · 2024–2025</p>
      </div>
    </article>
  </div>
</div>
