---
layout: post
title: Live Review — Sprint 1
permalink: /live-review/
codemirror: true
description: Individual and team checkpoints for the Sprint 1 Live Review — portfolio setup, SDLC steps, Unit 1-4 progress, unicorns, and office hours crew.
comments: false
---

<div class="live-review-page">

<div class="lr-intro">
  <p>
    This page is my checklist for the <strong>Live Review starting Thursday</strong>. It covers the
    <strong>Individual</strong> items I present on my own, and the <strong>Team</strong> items I cover
    with my CSSE crew. Instead of screenshots, I prove the coding pieces with <strong>live code runners</strong>
    you can run right here on the page — this is AP CSA, so they run <strong>Java</strong>.
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

<p>
  <strong>My proof that the Java toolchain works:</strong> the same JDK I installed for setup runs this
  live. Hit <strong>▶ Run</strong> — if it prints, my environment is real, not a screenshot.
</p>

{% capture setup_java %}
public class Setup {
    public static void main(String[] args) {
        System.out.println("Portfolio setup: COMPLETE");
        System.out.println("Toolchain: Git + GitHub + VSCode + Java (JDK)");
        System.out.println("Site: Jekyll -> GitHub Pages -> live");
    }
}
{% endcapture %}
{% include runners/code.html runner_id="setup-java" language="java" code=setup_java %}

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

<p>
  <strong>The SDLC loop as runnable code</strong> — this Java program is the same 7 steps as a list I can
  walk through out loud during the review:
</p>

{% capture sdlc_java %}
public class SDLC {
    public static void main(String[] args) {
        String[] steps = {
            "Plan", "Code", "Test", "Commit", "Push/Deploy", "Verify", "Reflect"
        };
        for (int i = 0; i < steps.length; i++) {
            System.out.println((i + 1) + ". " + steps[i]);
        }
        System.out.println("...then loop back to Plan for the next change.");
    }
}
{% endcapture %}
{% include runners/code.html runner_id="sdlc-java" language="java" code=sdlc_java %}

<hr>

<h2 id="units"><span class="lr-badge lr-badge-individual">Individual</span> 3. Progress on Unit 1–4 Capture</h2>

<p>Where I am in each unit of CSSE so far, and what I can point to as evidence during the review.</p>

<div class="unit-grid">
  <div class="unit-card">
    <div class="unit-card-head">
      <span class="unit-num">Unit 1</span>
      <span class="unit-title">Onboarding</span>
    </div>
    <p class="unit-desc">Getting Started → Essential Tools Setup → Scrum Agile Mini Project → Summative Coding Challenge → Retrospective.</p>
    <div class="unit-status">Status: <select class="unit-status-select"><option>Not Started</option><option selected>In Progress</option><option>Complete</option></select></div>
    <p class="unit-note">Tools installed, site deployed live, and on a Kanban board with my team. This whole page is my Unit 1 evidence.</p>
  </div>

  <div class="unit-card">
    <div class="unit-card-head">
      <span class="unit-num">Unit 2</span>
      <span class="unit-title">JavaScript Foundations & Student Teaching</span>
    </div>
    <p class="unit-desc">JS control structures, data types, classes/methods, and teaching a lesson to peers with a popcorn hack + homework.</p>
    <div class="unit-status">Status: <select class="unit-status-select"><option>Not Started</option><option selected>In Progress</option><option>Complete</option></select></div>
    <p class="unit-note">Working through control structures and classes; prepping a lesson + popcorn hack to teach a small group.</p>
  </div>

  <div class="unit-card">
    <div class="unit-card-head">
      <span class="unit-num">Unit 3</span>
      <span class="unit-title">Creating a Game for N@tM</span>
    </div>
    <p class="unit-desc">Game backgrounds, sprites/animation, player + NPCs, new mechanics, deploy and present at Night at the Museum.</p>
    <div class="unit-status">Status: <select class="unit-status-select"><option selected>Not Started</option><option>In Progress</option><option>Complete</option></select></div>
    <p class="unit-note">Next up. Planning the background + a player sprite first, then one new mechanic to demo at Night at the Museum.</p>
  </div>

  <div class="unit-card">
    <div class="unit-card-head">
      <span class="unit-num">Unit 4</span>
      <span class="unit-title">Ideating, Tinkering, Building & OOP</span>
    </div>
    <p class="unit-desc">Exploring the OCS GameEngine, working collaboratively, and applying OOP concepts in a team-built game.</p>
    <div class="unit-status">Status: <select class="unit-status-select"><option selected>Not Started</option><option>In Progress</option><option>Complete</option></select></div>
    <p class="unit-note">Not started yet. This is where AP CSA OOP (classes, objects, inheritance) plugs straight into the GameEngine.</p>
  </div>
</div>

<p>
  <strong>Live Unit 1–4 capture as one Java program.</strong> AP CSA is object-oriented, so I model each
  unit as an object with a status and print my progress — run it to see the capture:
</p>

{% capture units_java %}
public class Progress {
    // A tiny class = the OOP idea Unit 4 is built on
    static class Unit {
        int number;
        String title;
        String status;
        Unit(int number, String title, String status) {
            this.number = number;
            this.title = title;
            this.status = status;
        }
        void report() {
            System.out.println("Unit " + number + " (" + title + "): " + status);
        }
    }

    public static void main(String[] args) {
        Unit[] units = {
            new Unit(1, "Onboarding", "In Progress"),
            new Unit(2, "JavaScript Foundations", "In Progress"),
            new Unit(3, "Game for N@tM", "Not Started"),
            new Unit(4, "Tinkering, Building & OOP", "Not Started")
        };
        for (Unit u : units) {
            u.report();
        }
    }
}
{% endcapture %}
{% include runners/code.html runner_id="units-java" language="java" code=units_java %}

<hr>

<h2 id="unicorn"><span class="lr-badge lr-badge-individual">Individual</span> 4. What's My Unicorn?</h2>

<p>
  My <strong>unicorn</strong> is the one standout, one-of-a-kind thing I brought to each unit — the idea,
  fix, or feature that only I thought to add. Not "what did I complete," but "what made my version mine."
  <em>(These are my drafts to defend in the review — I'll swap in the exact detail for each as I finish the unit.)</em>
</p>

<div class="unicorn-grid">
  <div class="unicorn-card">
    <div class="unicorn-head">🦄 Unit 1</div>
    <p class="unicorn-answer">I turned my Live Review page into runnable proof — instead of screenshots, my portfolio setup is verified by Java code runners anyone can execute on the page.</p>
  </div>
  <div class="unicorn-card">
    <div class="unicorn-head">🦄 Unit 2</div>
    <p class="unicorn-answer">For student-teaching I built my popcorn hack as an interactive code runner, so the class learns the concept by editing and running it live instead of just watching slides.</p>
  </div>
  <div class="unicorn-card">
    <div class="unicorn-head">🦄 Unit 3</div>
    <p class="unicorn-answer">My N@tM game will ship one mechanic none of my teammates have — a custom interaction I designed myself — so the game reads as mine and not the template.</p>
  </div>
  <div class="unicorn-card">
    <div class="unicorn-head">🦄 Unit 4</div>
    <p class="unicorn-answer">In the GameEngine I'll add my own reusable class (clean OOP with inheritance) that the rest of the team can extend, so my code becomes shared infrastructure.</p>
  </div>
</div>

<hr>

<h2 id="office-hours"><span class="lr-badge lr-badge-team">Team</span> Office Hours — CSSE People</h2>

<p>
  <strong>Team activity, done live.</strong> I go to Office Hours to connect with other CSSE students outside
  my usual team — swapping fixes, comparing portfolios, and finding people to pair with. This is a talk-through
  item for the review; per the assignment, it doesn't need an artifact posted on the portfolio page itself, so
  there's nothing to capture here beyond showing up and naming the people I met.
</p>

<hr>

<h2 id="sprint1-friends"><span class="lr-badge lr-badge-team">Team</span> My CSSE Sprint 1 Friends</h2>

<p>
  The crew I went through Sprint 1 onboarding with. I'll introduce them live during the review — this is the
  team side of the checklist, presented in person rather than as an uploaded photo.
</p>

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

  /* --- Theme fix ---------------------------------------------------------
     The header light/dark toggle sets data-theme on <html> and swaps the
     --ocs-theme-* variables. The review cards already read those variables,
     but the surrounding content surface came from Minima and didn't move,
     so toggling looked like it "did nothing." Painting the content area
     from the same theme variables makes the whole page follow the toggle
     in both directions. --------------------------------------------------- */
  .page-content,
  .page-content .wrapper {
    background-color: var(--ocs-theme-bg, #0f1013);
  }

  .live-review-page a {
    color: var(--lr-accent);
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
    color: var(--lr-text);
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

  .unit-note {
    font-size: 0.82em;
    color: var(--lr-muted);
    margin: 10px 0 0;
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
    color: var(--lr-text);
    margin: 0;
  }
</style>
