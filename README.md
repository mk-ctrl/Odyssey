# Agentic Architecture Sprint
## Official Event Blueprint

**Odyssey Club — AI & Data Science Department**

---

A rapid-build, live-defense hackathon: teams vibe-code an application from a fresh problem statement, freeze code under a strict timer, and defend it under peer-driven QA *Crossfire* — with a hybrid AI + manual scoring system deciding the winner.

---

## Run of Show

### Phase 1 · The Vision _(First 10 Minutes)_

**Owner:** Head of Department (HOD)

Opening address covering the club's roadmap, goals for the academic year, and the vision for the AI & DS department. Sets a formal, high-stakes tone for the event.

---

### Phase 2 · Rules of Engagement _(5 Minutes)_

**Owner:** 3rd-Year Coordinators

Officially drop the Problem Statement (via GitHub repo / README). Explain the rules of the 35-minute sprint. Teams may strategize internally — some members build the app while others study requirements ahead of the bug-hunting phase.

---

### Phase 3 · The Build Sprint _(35 Minutes)_

Timer starts. Teams use their chosen AI IDEs (Cursor, Windsurf, Copilot, etc.) to generate the application.

**Enforcement:** Coordinators patrol the room to confirm teams are building from scratch, not reusing pre-existing code.

---

### Phase 4 · Code Freeze & Submission _(Strict 2 Minutes)_

When the timer hits `00:00`, coordinators announce **"Hands off keyboards."** The Google Form link is distributed. Teams have exactly 2 minutes to run the two mandatory AI prompts (see Section 3) to generate `functionality.md` and `chat_history.md`, then upload them.

*No team may begin QA testing until their form is submitted.*

---

### Phase 5 · The QA Crossfire _(15–20 Minutes)_

**The Rotation:** Two members from each team ("Breakers") rotate to a rival team's laptop.

**Rules for Breakers:**
- May **only** interact with the frontend / UI — no touching or reading source code.
- Actively try to break the app: empty submissions, rapid clicking, responsive-design checks.

**Point System (monitored by coordinators):**
- Bug found → Breaker raises hand → coordinator verifies on UI and logs it on paper.
- **Strike:** defending team immediately loses **5 points**.
- **Defense:** team gets 2–3 minutes to prompt their AI for a fix.
- **Recovery:** successful fix within the limit → penalty reduced to **−2.5**. Failed fix → full **−5** stands.

---

### Phase 6 · Wrap-up & Feedback

Event concludes. Coordinators distribute a feedback form on the sprint format while the back-end team preps submitted files for AI evaluation.

---

### Phase 7 · Result Validation & Official Announcement _(Post-Event)_

**Calculation:** Over the weekend, the back-end committee finalizes scores by running submitted `functionality.md` and `chat_history.md` files through the master AI evaluation prompt, then subtracting the manual QA penalties recorded on paper.

**HOD Clarification:** Finalized scorecards and winning team designations go to the HOD for official review and approval.

**Announcement:** Odyssey Club staff-in-charge officially post final results and declare winners in the respective class groups by Monday or Tuesday.

> **Why the delay?** Staging the announcement post-event keeps AI grading and QA penalty tallying accurate behind the scenes and protects the committee from on-the-floor disputes over the final score.

---

## The Final Evaluation System

The winner is determined by combining two grading pillars:

| Pillar | How It's Scored |
|--------|-----------------|
| **1. AI Automated Grading** (the baseline score) | The committee feeds submitted `functionality.md` and `chat_history.md` files into a master AI prompt, which evaluates prompting/token efficiency and how completely the team mapped problem-statement requirements into working features. |
| **2. QA Crossfire** (the deductions) | The baseline score is reduced by manual bug penalties tracked on paper by coordinators: **−5** per unsolved bug, **−2.5** per solved bug. |

### Final Score Formula

```
Final Score = AI Baseline Score − Total QA Penalties
```

---

## Mandatory Submission Prompts

During the 2-minute Code Freeze, coordinators must instruct all teams to copy and paste these **exact** prompts into their AI IDE, in order.

### Prompt 1 — The Functionality Manifest (`functionality.md`)

Forces the AI to output a structured, machine-readable report of the codebase state.

#### RUN THIS FIRST

```
SYSTEM COMMAND: Comprehensive Codebase Audit for Automated Evaluation.

You are acting as an internal state auditor. Analyze our entire current codebase. 
Generate a detailed, highly structured markdown document named `functionality.md`. 
This document will be evaluated by an AI judge, so technical precision is mandatory.

Format the output using the following exact headers and detail levels:

# TEAM FUNCTIONALITY MANIFEST

## 1. CORE FEATURES STATUS
* Bulleted list of exact features from the problem statement that are 100% functional 
  and bug-free in the UI.
* Detail the specific logic/state management powering each working feature.

## 2. MISSING LOGIC & KNOWN BUGS
* List features attempted but broken, throwing errors, or incomplete.
* List core requirements from the problem statement that were not implemented.

## 3. UI, STATE & EDGE CASES
* Explain how frontend state is managed.
* Describe handling of invalid user inputs / edge cases.
* Confirm mobile-viewport responsiveness based on the CSS provided.

## 4. DEPENDENCY TREE
* List all frameworks, libraries, and external tools actually used in the codebase.

WARNING: Do not hallucinate. Do not claim a feature works if the underlying logic 
is missing. Falsified claims will result in heavy penalties during the live UI QA testing.
```

---

### Prompt 2 — The Token & Strategy Audit (`chat_history.md`)

Run immediately after the manifest — extracts both user inputs and AI outputs for token-efficiency and prompting-strategy evaluation.

#### RUN THIS SECOND

```
SYSTEM COMMAND: Full Session Transcript Export.

I need to export the entire interaction history of this current session so an 
external auditor can evaluate our token efficiency, iteration speed, and prompting strategy.

Generate a markdown document named `chat_history.md` that includes BOTH my exact inputs 
(prompts) AND your complete outputs (code responses and text) in chronological order, 
starting from the very first message.

Format it exactly like this:

### User Prompt [Number]
[My exact input text]

### AI Response [Number]
[Your exact output text/code]

CRITICAL REQUIREMENT: Do not summarize our conversation. Do not skip any iterations, 
errors, or debugging loops. Output the raw data sequentially.
```

---

## Submission form link
https://forms.gle/zupUT1DMYNG2ZTPbA

---

