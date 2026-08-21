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
  <a href="#unit1-mcq">Unit 1 MCQ</a>
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

<h2 id="unit1-mcq"><span class="lr-badge lr-badge-individual">Individual</span> Unit 1 MCQ — Primitive Types</h2>

<p>
  This is our class <strong>Unit 1 Quiz</strong> (Primitive Types) from the CSA MCQ notebooks, rebuilt so it's
  actually <strong>takeable</strong> right here. Pick an answer for each question and hit <strong>Submit</strong>
  to score it — each question turns green/red and shows why. Then run the Java underneath to see the same
  primitive-type concepts execute for real.
</p>

<div class="u1-quiz" id="u1-quiz">
  <form onsubmit="return false;" autocomplete="off">

    <div class="u1-q" data-answer="b">
      <div class="u1-q-title">1. Which of the following is a valid declaration of a variable of type <code>int</code> in Java?</div>
      <label class="u1-opt"><input type="radio" name="u1q1" value="a"> <span>a) <code>int 123variable;</code></span></label>
      <label class="u1-opt"><input type="radio" name="u1q1" value="b"> <span>b) <code>int variable123;</code></span></label>
      <label class="u1-opt"><input type="radio" name="u1q1" value="c"> <span>c) <code>int variable#123;</code></span></label>
      <label class="u1-opt"><input type="radio" name="u1q1" value="d"> <span>d) <code>int variable 123;</code></span></label>
      <div class="u1-explain">Answer: <strong>b</strong>. Java identifiers can't start with a digit, can't contain symbols like <code>#</code>, and can't contain spaces. <code>variable123</code> (camelCase) is the only legal name.</div>
    </div>

    <div class="u1-q" data-answer="c">
      <div class="u1-q-title">2. What is the value of the following expression in Java: <code>5 / 2</code>?</div>
      <label class="u1-opt"><input type="radio" name="u1q2" value="a"> <span>a) 2.5</span></label>
      <label class="u1-opt"><input type="radio" name="u1q2" value="b"> <span>b) 3</span></label>
      <label class="u1-opt"><input type="radio" name="u1q2" value="c"> <span>c) 2</span></label>
      <label class="u1-opt"><input type="radio" name="u1q2" value="d"> <span>d) 2.0</span></label>
      <div class="u1-explain">Answer: <strong>c</strong>. Dividing two <code>int</code>s does integer division, which truncates toward zero — so <code>5 / 2</code> is <code>2</code>, not <code>2.5</code>. You'd need <code>5.0 / 2</code> to get <code>2.5</code>.</div>
    </div>

    <div class="u1-q" data-answer="a">
      <div class="u1-q-title">3. Which primitive type is used to represent a single character in Java?</div>
      <label class="u1-opt"><input type="radio" name="u1q3" value="a"> <span>a) <code>char</code></span></label>
      <label class="u1-opt"><input type="radio" name="u1q3" value="b"> <span>b) <code>String</code></span></label>
      <label class="u1-opt"><input type="radio" name="u1q3" value="c"> <span>c) <code>int</code></span></label>
      <label class="u1-opt"><input type="radio" name="u1q3" value="d"> <span>d) <code>byte</code></span></label>
      <div class="u1-explain">Answer: <strong>a</strong>. <code>char</code> holds one character in single quotes (e.g. <code>'A'</code>). <code>String</code> is a reference type for text, not a primitive.</div>
    </div>

    <div class="u1-quiz-controls">
      <button type="button" class="u1-btn u1-submit" onclick="gradeUnit1Quiz()">Submit Quiz</button>
      <button type="button" class="u1-btn u1-reset" onclick="resetUnit1Quiz()">Reset</button>
    </div>
  </form>
  <div class="u1-result" id="u1-result" role="status" aria-live="polite"></div>
</div>

<p>
  <strong>Now run it.</strong> This is Question 4's primitive-vs-reference example plus the <code>5 / 2</code>
  behavior from Question 2 — press <strong>▶ Run</strong> to prove the answers in real Java:
</p>

{% capture mcq_java %}
public class PrimitivesDemo {
    // Reference type: a Person object lives on the heap
    static class Person {
        String name;
        int age;
        Person(String name, int age) {
            this.name = name;
            this.age = age;
        }
    }

    public static void main(String[] args) {
        // Q2: integer division truncates
        System.out.println("5 / 2   = " + (5 / 2));     // 2 (int division)
        System.out.println("5.0 / 2 = " + (5.0 / 2));   // 2.5 (double division)

        // Q3: char is a primitive holding ONE character
        char grade = 'A';
        System.out.println("char grade = " + grade);

        // Q4: reference types share the same object in memory
        Person person1 = new Person("Carl", 25);
        Person person3 = person1;                 // points to the SAME object
        person3.age = 99;
        System.out.println("person1.age = " + person1.age + " (changed through person3)");
        System.out.println("person1 == person3 ? " + (person1 == person3)); // true
    }
}
{% endcapture %}
{% include runners/code.html runner_id="unit1-mcq-java" language="java" code=mcq_java %}

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

  /* --- Unit 1 interactive MCQ --- */
  .u1-quiz {
    background: var(--lr-bg);
    border: 1px solid var(--lr-border);
    border-radius: 12px;
    padding: 18px;
    margin: 16px 0;
  }

  .u1-q {
    border: 1px solid var(--lr-border);
    border-radius: 10px;
    padding: 14px 16px;
    margin-bottom: 14px;
    transition: border-color 0.2s;
  }

  .u1-q-title {
    font-weight: 700;
    margin-bottom: 10px;
  }

  .u1-opt {
    display: flex;
    align-items: flex-start;
    gap: 8px;
    padding: 7px 10px;
    border: 1px solid transparent;
    border-radius: 8px;
    cursor: pointer;
    color: var(--lr-text);
  }

  .u1-opt:hover {
    border-color: var(--lr-border);
  }

  .u1-opt input {
    margin-top: 3px;
    accent-color: var(--lr-accent);
  }

  /* Feedback states applied after Submit */
  .u1-opt.is-correct {
    border-color: #4caf50;
    background: rgba(76, 175, 80, 0.12);
  }

  .u1-opt.is-wrong {
    border-color: #e05656;
    background: rgba(224, 86, 86, 0.12);
  }

  .u1-explain {
    display: none;
    font-size: 0.85em;
    color: var(--lr-muted);
    margin-top: 8px;
    padding-top: 8px;
    border-top: 1px dashed var(--lr-border);
  }

  .u1-q.answered .u1-explain {
    display: block;
  }

  .u1-quiz-controls {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
    margin-top: 4px;
  }

  .u1-btn {
    border-radius: 8px;
    padding: 9px 18px;
    font-weight: 700;
    cursor: pointer;
    border: 1px solid var(--lr-border);
  }

  .u1-submit {
    background: var(--lr-accent);
    color: #1a1a1a;
    border-color: var(--lr-accent);
  }

  .u1-reset {
    background: transparent;
    color: var(--lr-text);
  }

  .u1-result {
    display: none;
    margin-top: 14px;
    padding: 14px 16px;
    border-radius: 10px;
    border: 1px solid var(--lr-border);
    font-weight: 700;
    text-align: center;
  }

  .u1-result.show {
    display: block;
  }
</style>

<script>
  (function () {
    function optionLabels(qEl) {
      return Array.prototype.slice.call(qEl.querySelectorAll('.u1-opt'));
    }

    window.gradeUnit1Quiz = function () {
      var quiz = document.getElementById('u1-quiz');
      if (!quiz) return;
      var questions = quiz.querySelectorAll('.u1-q');
      var score = 0;
      var unanswered = 0;

      questions.forEach(function (q) {
        var correct = q.getAttribute('data-answer');
        var labels = optionLabels(q);
        var picked = null;

        labels.forEach(function (label) {
          label.classList.remove('is-correct', 'is-wrong');
          var input = label.querySelector('input');
          if (input && input.checked) picked = input.value;
        });

        if (!picked) unanswered++;

        labels.forEach(function (label) {
          var input = label.querySelector('input');
          if (!input) return;
          if (input.value === correct) {
            label.classList.add('is-correct');
          } else if (input.checked) {
            label.classList.add('is-wrong');
          }
        });

        q.classList.add('answered');
        if (picked === correct) score++;
      });

      var total = questions.length;
      var result = document.getElementById('u1-result');
      var msg;
      if (score === total) {
        msg = '🌟 ' + score + ' / ' + total + ' — perfect! You know your primitive types.';
      } else if (score >= Math.ceil(total / 2)) {
        msg = '👍 ' + score + ' / ' + total + ' — solid. Read the highlighted answers to lock it in.';
      } else {
        msg = '📘 ' + score + ' / ' + total + ' — review the explanations under each question and retry.';
      }
      if (unanswered > 0) {
        msg += ' (' + unanswered + ' left blank counted as wrong.)';
      }
      result.textContent = msg;
      result.classList.add('show');
      result.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
    };

    window.resetUnit1Quiz = function () {
      var quiz = document.getElementById('u1-quiz');
      if (!quiz) return;
      quiz.querySelectorAll('input[type="radio"]').forEach(function (i) { i.checked = false; });
      quiz.querySelectorAll('.u1-opt').forEach(function (l) { l.classList.remove('is-correct', 'is-wrong'); });
      quiz.querySelectorAll('.u1-q').forEach(function (q) { q.classList.remove('answered'); });
      var result = document.getElementById('u1-result');
      result.classList.remove('show');
      result.textContent = '';
    };
  })();
</script>
