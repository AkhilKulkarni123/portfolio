---
layout: post
title: Live Review — Sprint 1
permalink: /live-review/
description: Individual and team checkpoints for the Sprint 1 Live Review — portfolio setup, SDLC steps, Unit 1-4 progress, unicorns, and office hours crew.
comments: false
---

<div class="live-review-page">

<div class="lr-intro">
  <p>
    This page is my checklist for the <strong>Live Review starting Thursday</strong>. It covers the
    <strong>Individual</strong> items I present on my own, and the <strong>Team</strong> items I cover
    with my CSSE crew. Screenshots are marked with a <span class="lr-slot-tag">📷 proof slot</span> —
    I'll drop my own images into those once I have them.
  </p>
</div>

<div class="lr-toc">
  <a href="#setup">1. Portfolio Setup</a>
  <a href="#sdlc">2. SDLC Steps</a>
  <a href="#units">3. Unit 1–4 Progress</a>
  <a href="#unicorn">4. My Unicorn</a>
  <a href="#office-hours">Office Hours (Team)</a>
  <a href="#sprint1-friends">Sprint 1 Friends</a>
</div>

<hr>

<h2 id="setup"><span class="lr-badge lr-badge-individual">Individual</span> 1. My Portfolio Setup</h2>

<p>
  My portfolio is forked from the Open Coding Society <a href="https://github.com/Open-Coding-Society/pages" target="_blank" rel="noopener">pages</a>
  template and built with Jekyll + GitHub Pages. Getting from "empty fork" to "live site" meant setting up
  the same local toolchain the <a href="{{ site.baseurl }}/rpg/game">CS Pathway game's</a> "Mission Tooling"
  level walks through: Git, GitHub, VSCode, a terminal, and Java for the tools that need it.
</p>

<div class="lr-checklist">
  <div class="lr-check-item">✅ Forked/used-the-template on GitHub, cloned it locally</div>
  <div class="lr-check-item">✅ Installed VSCode, Git, and a terminal (Linux/macOS/Windows+WSL)</div>
  <div class="lr-check-item">✅ Installed Java (JDK) + verified with <code>java -version</code></div>
  <div class="lr-check-item">✅ Ran the site locally (<code>bundle exec jekyll serve</code> / <code>make</code>)</div>
  <div class="lr-check-item">✅ Edited <code>_config.yml</code> with my own title, name, and GitHub info</div>
  <div class="lr-check-item">✅ Pushed a change and confirmed GitHub Pages rebuilt the live site</div>
</div>

<p><em>Reference: how the general fork → configure → deploy flow looks (shared class screenshots):</em></p>

<div class="lr-ref-row">
  <figure>
    <img src="{{ site.baseurl }}/images/tools/use-this-template.png" alt="Use this template on GitHub">
    <figcaption>Fork / use template</figcaption>
  </figure>
  <figure>
    <img src="{{ site.baseurl }}/images/tools/editconfig-yml.png" alt="Editing _config.yml">
    <figcaption>Edit _config.yml</figcaption>
  </figure>
  <figure>
    <img src="{{ site.baseurl }}/images/tools/deploygithubpages.png" alt="Deploy to GitHub Pages">
    <figcaption>Deploy to Pages</figcaption>
  </figure>
</div>

<p><strong>My proof</strong> — my own toolset and setup screenshots go here:</p>

<div class="lr-proof-grid">
  <div class="proof-slot">
    📷 Add screenshot here
    <small>e.g. VSCode + terminal open side by side</small>
    <!-- Replace this box with: <img src="{{ site.baseurl }}/images/live-review/my-toolset.png" alt="My dev toolset"> -->
  </div>
  <div class="proof-slot">
    📷 Add screenshot here
    <small><code>java -version</code> output</small>
    <!-- Replace this box with: <img src="{{ site.baseurl }}/images/live-review/java-version.png" alt="Java installed"> -->
  </div>
  <div class="proof-slot">
    📷 Add screenshot here
    <small>My live GitHub Pages site</small>
    <!-- Replace this box with: <img src="{{ site.baseurl }}/images/live-review/live-site.png" alt="My live portfolio site"> -->
  </div>
</div>

<hr>

<h2 id="sdlc"><span class="lr-badge lr-badge-individual">Individual</span> 2. SDLC Steps for Updating My Portfolio</h2>

<p>
  Every change I make to my portfolio follows the same Software Development Life Cycle loop, just scoped
  small: plan the change, write it, ship it, check it worked, and use what I learn to plan the next one.
</p>

<div class="lr-sdlc-track">
  <div class="lr-sdlc-step">
    <div class="lr-sdlc-num">1</div>
    <div class="lr-sdlc-title">Plan</div>
    <div class="lr-sdlc-body">Pick the change (fix a bug, add a page, update a project). Check the Kanban/issue board.</div>
  </div>
  <div class="lr-sdlc-step">
    <div class="lr-sdlc-num">2</div>
    <div class="lr-sdlc-title">Code</div>
    <div class="lr-sdlc-body">Edit locally in VSCode — Markdown, HTML, CSS, or JavaScript.</div>
  </div>
  <div class="lr-sdlc-step">
    <div class="lr-sdlc-num">3</div>
    <div class="lr-sdlc-title">Test</div>
    <div class="lr-sdlc-body">Run the site locally and check the page in the browser before shipping.</div>
  </div>
  <div class="lr-sdlc-step">
    <div class="lr-sdlc-num">4</div>
    <div class="lr-sdlc-title">Commit</div>
    <div class="lr-sdlc-body"><code>git add</code>, <code>git commit -m "..."</code> — a clear message per change.</div>
  </div>
  <div class="lr-sdlc-step">
    <div class="lr-sdlc-num">5</div>
    <div class="lr-sdlc-title">Push / Deploy</div>
    <div class="lr-sdlc-body"><code>git push</code> → GitHub Actions builds the Jekyll site → GitHub Pages goes live.</div>
  </div>
  <div class="lr-sdlc-step">
    <div class="lr-sdlc-num">6</div>
    <div class="lr-sdlc-title">Verify</div>
    <div class="lr-sdlc-body">Reload the live URL, confirm the build succeeded and the change is really there.</div>
  </div>
  <div class="lr-sdlc-step">
    <div class="lr-sdlc-num">7</div>
    <div class="lr-sdlc-title">Reflect</div>
    <div class="lr-sdlc-body">Note what broke or was slow, and feed it into the next Plan step.</div>
  </div>
</div>

<div class="lr-ref-row">
  <figure>
    <img src="{{ site.baseurl }}/images/tools/makechangescommit.png" alt="Make changes and commit">
    <figcaption>Code → Commit</figcaption>
  </figure>
  <figure>
    <img src="{{ site.baseurl }}/images/tools/changegithubpagesbuild.png" alt="GitHub Pages build running">
    <figcaption>Push → Build</figcaption>
  </figure>
</div>

<p><strong>My proof</strong> — a screenshot of my own commit history or a passing build goes here:</p>

<div class="lr-proof-grid">
  <div class="proof-slot lr-proof-wide">
    📷 Add screenshot here
    <small>My git log / commit history, or a green GitHub Actions build</small>
    <!-- Replace this box with: <img src="{{ site.baseurl }}/images/live-review/my-commits.png" alt="My commit history"> -->
  </div>
</div>

<hr>

<h2 id="units"><span class="lr-badge lr-badge-individual">Individual</span> 3. Progress on Unit 1–4 Capture</h2>

<p>Where I am in each unit of CSSE so far. I'll keep this updated as I capture more evidence for each one.</p>

<div class="unit-grid">
  <div class="unit-card">
    <div class="unit-card-head">
      <span class="unit-num">Unit 1</span>
      <span class="unit-title">Onboarding</span>
    </div>
    <p class="unit-desc">Getting Started → Essential Tools Setup → Scrum Agile Mini Project → Summative Coding Challenge → Retrospective.</p>
    <div class="unit-status">Status: <select class="unit-status-select"><option>Not Started</option><option selected>In Progress</option><option>Complete</option></select></div>
    <div class="proof-slot proof-slot-small">
      📷 Add capture here
      <!-- <img src="{{ site.baseurl }}/images/live-review/unit1-capture.png" alt="Unit 1 capture"> -->
    </div>
  </div>

  <div class="unit-card">
    <div class="unit-card-head">
      <span class="unit-num">Unit 2</span>
      <span class="unit-title">JavaScript Foundations & Student Teaching</span>
    </div>
    <p class="unit-desc">JS control structures, data types, classes/methods, and teaching a lesson to peers with a popcorn hack + homework.</p>
    <div class="unit-status">Status: <select class="unit-status-select"><option selected>Not Started</option><option>In Progress</option><option>Complete</option></select></div>
    <div class="proof-slot proof-slot-small">
      📷 Add capture here
      <!-- <img src="{{ site.baseurl }}/images/live-review/unit2-capture.png" alt="Unit 2 capture"> -->
    </div>
  </div>

  <div class="unit-card">
    <div class="unit-card-head">
      <span class="unit-num">Unit 3</span>
      <span class="unit-title">Creating a Game for N@tM</span>
    </div>
    <p class="unit-desc">Game backgrounds, sprites/animation, player + NPCs, new mechanics, deploy and present at Night at the Museum.</p>
    <div class="unit-status">Status: <select class="unit-status-select"><option selected>Not Started</option><option>In Progress</option><option>Complete</option></select></div>
    <div class="proof-slot proof-slot-small">
      📷 Add capture here
      <!-- <img src="{{ site.baseurl }}/images/live-review/unit3-capture.png" alt="Unit 3 capture"> -->
    </div>
  </div>

  <div class="unit-card">
    <div class="unit-card-head">
      <span class="unit-num">Unit 4</span>
      <span class="unit-title">Ideating, Tinkering, Building & OOP</span>
    </div>
    <p class="unit-desc">Exploring the OCS GameEngine, working collaboratively, and applying OOP concepts in a team-built game.</p>
    <div class="unit-status">Status: <select class="unit-status-select"><option selected>Not Started</option><option>In Progress</option><option>Complete</option></select></div>
    <div class="proof-slot proof-slot-small">
      📷 Add capture here
      <!-- <img src="{{ site.baseurl }}/images/live-review/unit4-capture.png" alt="Unit 4 capture"> -->
    </div>
  </div>
</div>

<hr>

<h2 id="unicorn"><span class="lr-badge lr-badge-individual">Individual</span> 4. What's My Unicorn?</h2>

<p>
  My <strong>unicorn</strong> is the one standout, one-of-a-kind thing I brought to each unit — the idea,
  fix, or feature that only I thought to add. Not "what did I complete," but "what made my version mine."
</p>

<div class="unicorn-grid">
  <div class="unicorn-card">
    <div class="unicorn-head">🦄 Unit 1</div>
    <p class="unicorn-answer">[Your unicorn for Unit 1 goes here]</p>
  </div>
  <div class="unicorn-card">
    <div class="unicorn-head">🦄 Unit 2</div>
    <p class="unicorn-answer">[Your unicorn for Unit 2 goes here]</p>
  </div>
  <div class="unicorn-card">
    <div class="unicorn-head">🦄 Unit 3</div>
    <p class="unicorn-answer">[Your unicorn for Unit 3 goes here]</p>
  </div>
  <div class="unicorn-card">
    <div class="unicorn-head">🦄 Unit 4</div>
    <p class="unicorn-answer">[Your unicorn for Unit 4 goes here]</p>
  </div>
</div>

<hr>

<h2 id="office-hours"><span class="lr-badge lr-badge-team">Team</span> Office Hours — CSSE People I Found</h2>

<p>
  Went to office hours and connected with other CSSE students outside my usual team. Notes and names go below.
</p>

<ul class="lr-people-list">
  <li>[Name] — [what we talked about / helped with]</li>
  <li>[Name] — [what we talked about / helped with]</li>
  <li>[Name] — [what we talked about / helped with]</li>
</ul>

<div class="lr-proof-grid">
  <div class="proof-slot lr-proof-wide">
    📷 Add screenshot here
    <small>Office hours photo or chat/Slack proof</small>
    <!-- Replace this box with: <img src="{{ site.baseurl }}/images/live-review/office-hours.png" alt="Office hours with CSSE people"> -->
  </div>
</div>

<hr>

<h2 id="sprint1-friends"><span class="lr-badge lr-badge-team">Team</span> My CSSE Sprint 1 Friends</h2>

<p>The crew I went through Sprint 1 onboarding with.</p>

<div class="image-gallery lr-friends-gallery">
  <div class="proof-slot proof-slot-gallery">
    📷 Add photo here
    <!-- Replace this box with: <img src="{{ site.baseurl }}/images/live-review/sprint1-friends.jpg" alt="My Sprint 1 CSSE friends"> -->
  </div>
</div>

</div>

<style>
  .live-review-page {
    --lr-bg: var(--ocs-theme-card, #1c1d24);
    --lr-border: var(--ocs-theme-border, #33353f);
    --lr-text: var(--ocs-theme-text, #f2f2f2);
    --lr-muted: var(--ocs-theme-muted, #a8a8b3);
    --lr-accent: var(--ocs-theme-accent, #FA8072);
    color: var(--lr-text);
    max-width: 960px;
    margin: 0 auto;
  }

  .live-review-page hr {
    border: none;
    border-top: 1px solid var(--lr-border);
    margin: 32px 0;
  }

  .live-review-page h2 {
    display: flex;
    align-items: center;
    gap: 10px;
    flex-wrap: wrap;
  }

  .lr-badge {
    font-size: 0.6em;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.04em;
    padding: 3px 10px;
    border-radius: 999px;
    border: 1px solid var(--lr-border);
  }

  .lr-badge-individual {
    color: var(--lr-accent);
    border-color: var(--lr-accent);
  }

  .lr-badge-team {
    color: #6db3f2;
    border-color: #6db3f2;
  }

  .lr-intro {
    background: var(--lr-bg);
    border: 1px solid var(--lr-border);
    border-radius: 10px;
    padding: 16px 20px;
  }

  .lr-slot-tag {
    color: var(--lr-accent);
    font-weight: 600;
  }

  .lr-toc {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin: 16px 0;
  }

  .lr-toc a {
    font-size: 0.85em;
    padding: 6px 12px;
    border-radius: 999px;
    border: 1px solid var(--lr-border);
    text-decoration: none;
    color: var(--lr-text);
  }

  .lr-toc a:hover {
    border-color: var(--lr-accent);
    color: var(--lr-accent);
  }

  .lr-checklist {
    display: grid;
    gap: 8px;
    margin: 16px 0;
  }

  .lr-check-item {
    background: var(--lr-bg);
    border: 1px solid var(--lr-border);
    border-radius: 8px;
    padding: 10px 14px;
  }

  .lr-ref-row {
    display: flex;
    flex-wrap: wrap;
    gap: 16px;
    margin: 16px 0;
  }

  .lr-ref-row figure {
    margin: 0;
    flex: 1 1 220px;
    max-width: 260px;
  }

  .lr-ref-row img {
    width: 100%;
    border-radius: 8px;
    border: 1px solid var(--lr-border);
    display: block;
  }

  .lr-ref-row figcaption {
    font-size: 0.8em;
    color: var(--lr-muted);
    text-align: center;
    margin-top: 4px;
  }

  .lr-proof-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 16px;
    margin: 16px 0;
  }

  .proof-slot {
    border: 2px dashed var(--lr-border);
    border-radius: 10px;
    padding: 28px 16px;
    text-align: center;
    color: var(--lr-muted);
    font-size: 0.95em;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 6px;
    min-height: 110px;
  }

  .proof-slot small {
    color: var(--lr-muted);
    font-size: 0.8em;
  }

  .lr-proof-wide {
    grid-column: 1 / -1;
  }

  .proof-slot-small {
    min-height: 70px;
    padding: 16px 10px;
    margin-top: 10px;
  }

  .proof-slot-gallery {
    min-height: 160px;
    min-width: 220px;
  }

  .lr-sdlc-track {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    gap: 12px;
    margin: 20px 0;
  }

  .lr-sdlc-step {
    background: var(--lr-bg);
    border: 1px solid var(--lr-border);
    border-radius: 10px;
    padding: 14px;
    position: relative;
  }

  .lr-sdlc-num {
    width: 26px;
    height: 26px;
    border-radius: 50%;
    background: var(--lr-accent);
    color: #1a1a1a;
    font-weight: 700;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 8px;
  }

  .lr-sdlc-title {
    font-weight: 700;
    margin-bottom: 4px;
  }

  .lr-sdlc-body {
    font-size: 0.85em;
    color: var(--lr-muted);
  }

  .unit-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 16px;
    margin: 16px 0;
  }

  .unit-card {
    background: var(--lr-bg);
    border: 1px solid var(--lr-border);
    border-radius: 12px;
    padding: 16px;
  }

  .unit-card-head {
    display: flex;
    flex-direction: column;
    gap: 2px;
    margin-bottom: 8px;
  }

  .unit-num {
    color: var(--lr-accent);
    font-weight: 700;
    font-size: 0.85em;
    text-transform: uppercase;
    letter-spacing: 0.04em;
  }

  .unit-title {
    font-weight: 700;
  }

  .unit-desc {
    font-size: 0.85em;
    color: var(--lr-muted);
    margin: 6px 0 10px;
  }

  .unit-status {
    font-size: 0.85em;
  }

  .unit-status-select {
    background: transparent;
    color: var(--lr-text);
    border: 1px solid var(--lr-border);
    border-radius: 6px;
    padding: 3px 6px;
  }

  .unicorn-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 16px;
    margin: 16px 0;
  }

  .unicorn-card {
    background: var(--lr-bg);
    border: 1px solid var(--lr-accent);
    border-radius: 12px;
    padding: 16px;
  }

  .unicorn-head {
    font-weight: 700;
    margin-bottom: 8px;
  }

  .unicorn-answer {
    color: var(--lr-muted);
    font-style: italic;
    margin: 0;
  }

  .lr-people-list {
    background: var(--lr-bg);
    border: 1px solid var(--lr-border);
    border-radius: 10px;
    padding: 16px 16px 16px 36px;
  }

  .lr-friends-gallery {
    gap: 16px;
  }
</style>

