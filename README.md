

# ODYSSEY: AGENTIC ARCHITECTURE SPRINT

**TIME ALLOCATION:** 35 Minutes
**SUBMISSION WINDOW:** 2 Minutes

Welcome to Day Zero. You are here to demonstrate architectural thinking, AI command precision, and rapid debugging. 

---

## 🕒 THE TIMELINE
* **00:00 - 35:00:** The Build Phase.
* **35:00 - 37:00:** The Code Freeze & Submission Drill (Strict 2-minute window).
* **37:00 - End:** The QA Crossfire. 

---

## 🎯 THE PROBLEM STATEMENT: Agentic Task Orchestrator

You must build a responsive, single-page dashboard that simulates a multi-agent task orchestration system. Your application must handle state transitions, real-time filtering, and simulated asynchronous processing.

### 1. Core UI Requirements
* **The Kanban Board:** Create a three-column layout: `Pending Tasks`, `Agents Processing`, and `Completed Logs`.
* **Task Creation:** A text input area where users can type a new task and add it to the `Pending Tasks` column. 
* **Agent Assignment (The Simulation):** 
  * Every task in the `Pending Tasks` column must have a "Deploy Agent" button.
  * Clicking this moves the task to `Agents Processing`.
  * **The Catch:** Once in `Agents Processing`, the task must display a loading spinner/indicator for exactly **3 seconds**.
  * After 3 seconds, it must automatically move to the `Completed Logs` column.
* **Master Filter:** A dropdown or toggle that allows the user to filter tasks by `priority` (High, Medium, Low) across all columns simultaneously.

### 2. Mandatory Initial Data (Mock State)
Your application must load with this exact initial state. Do not start with an empty board.



---

## 🛠️ TECH STACK CONSTRAINTS

* **Bring Your Own Stack:** You may use any language, framework, or UI library you are comfortable with (React, Python, Next.js, HTML/JS, etc.). Any AI IDE or LLM is permitted.
* **The Golden Rule:** You must build this from scratch using your AI during the 35 minutes. You may not import personal templates, pre-existing projects, or code written prior to this event.

---

## ⚔️ THE QA CROSSFIRE (Rules of Engagement)

At minute 37:00, 2 members of your team ("Breakers") will rotate to a rival team's laptop.

**What the Breakers will test:**

1. **Crash Testing:** Can they break your UI by submitting empty tasks?
2. **Race Conditions:** What happens if they click "Deploy Agent" on 5 tasks in less than a second? Does your 3-second timer break?
3. **State Integrity:** Does switching the Master Filter while a task is in the `Processing` column crash the app or hide the task permanently?
4. **Responsive Design:** Does the application break horizontally when resized to a mobile viewport?

* **The Strike:** Every verified bug found by a Breaker costs your team **-5 Points**.
* **The Defense:** If your team can prompt your AI to patch the bug and push it live within **2 minutes**, you recover half the penalty (**+2.5 points**).

---

## 🛑 CODE FREEZE & SUBMISSION PROTOCOL

At exactly **35:00**, all coding must stop. You have exactly 2 minutes to generate your audit files and submit them. **Failure to submit by 37:00 results in instant disqualification.**

### Step 1: Generate `manifest.md`

Paste this exact prompt into your AI:

> `SYSTEM COMMAND: Code Freeze Audit. Analyze all the code in our current workspace. Generate a strict, honest report of our final application state. Format the output exactly with markdown headers: 1. FULLY FUNCTIONAL, 2. INCOMPLETE / BROKEN, 3. TECH STACK & DEPENDENCIES. WARNING TO AI: Do not lie. If you list a feature as functional and it crashes during QA, we suffer severe penalties.`

### Step 2: Generate `prompts.md`

Paste this exact prompt into your AI immediately after the manifest is generated:

> `SYSTEM COMMAND: Prompt History Extraction. Scan this entire chat session from the first message. Output a single markdown block containing EVERY prompt I have given you, in chronological order. Format with "### Prompt [Number]" followed by my text. Do not include your responses or summarize.`

### Step 3: Submit

Upload both `manifest.md` and `prompts.md` to the official Google Form provided by the Committee.

```

```
