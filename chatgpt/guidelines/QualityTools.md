# AI Coding Quality Tools Reference

## Purpose

This guide lists core quality tools from Six Sigma, Lean, and general quality management — adapted for software engineering or AI coding workflows — plus a simple high-level approach for how to apply them.

---

## Core Quality Tools for AI Coding

### 1. 5 Whys

* **What it is:** Iteratively asking “Why?” to drill down to the root cause of a defect.
* **Use it for:** Any unexpected bug, failure, or undesirable result.
* **Tip:** Document the chain of reasoning so you don’t stop at symptoms.

---

### 2. Cause and Effect Diagram (Fishbone / Ishikawa)

* **What it is:** A visual brainstorming tool to categorize possible causes under broad headings.
* **Use it for:** Complex bugs or recurring failures that have multiple possible causes.
* **Common categories for software:**

  * People (skills, human error)
  * Methods (algorithms, logic)
  * Machines (hardware, environments)
  * Materials (dependencies, data)
  * Measurements (tests, logs)
  * Environment (OS, network)

---

### 3. Plan-Do-Check-Act (PDCA Cycle)

* **What it is:** A simple iterative cycle for testing and implementing fixes.
* **Use it for:** Developing, verifying, and deploying changes safely.

  * Plan: Define hypothesis or fix.
  * Do: Implement the fix in a controlled way.
  * Check: Validate results (tests, metrics).
  * Act: Standardize if successful or try again.

---

### 4. Root Cause Verification Matrix

* **What it is:** A table to check if suspected causes are real.
* **Use it for:** Verifying your root cause hypotheses before spending effort on fixes.
* **Simple format:**

  | Suspected Cause | Verification Method | Evidence Result |
  | --------------- | ------------------- | --------------- |

---

### 5. Failure Modes and Effects Analysis (FMEA)

* **What it is:** A structured way to identify potential failure points, rank their risk, and prioritize preventive actions.
* **Use it for:** Critical modules or complex systems where failure would be high impact.
* **Key parts:** Severity, Occurrence, Detection → Risk Priority Number (RPN).

---

### 6. Design of Experiments (DOE) — Basic Version

* **What it is:** Systematically changing inputs to see what impacts outputs.
* **Use it for:** Testing multiple changes at once (e.g., config settings, parameter tuning).
* **Keep it simple:** For code, run A/B tests or toggle feature flags to measure impact.

---

## High-Level Steps for Applying Quality Tools

### Step 1: Define the Problem Clearly

* Write a clear, concise problem statement.
* Identify measurable impact: frequency, severity, cost.

### Step 2: Understand the Process

* Map out the relevant flow (e.g., SIPOC or workflow diagram).
* Identify where the defect or inefficiency occurs.

### Step 3: Analyze Root Causes

* Use 5 Whys to dig deep.
* Use Fishbone Diagram for brainstorming.
* Use Root Cause Verification Matrix to confirm.

### Step 4: Prioritize and Plan Solutions

* Use Pareto Charts to see which causes are most impactful.
* Rank risks with FMEA if needed.
* Select a fix; plan it using PDCA.

### Step 5: Test and Verify

* Use PDCA: implement fixes in safe test branches.
* Validate results with Run Charts, test coverage, and regression tests.

### Step 6: Control and Prevent Recurrence

* Document new learnings and fixes.
* Automate tests where possible.
* Update processes, checklists, or CI pipelines to catch similar issues early.

---

## Quick Reference: When to Use Each Tool

| Tool                    | When to Use                                    |
| ----------------------- | ---------------------------------------------- |
| 5 Whys                  | Any single bug or defect                       |
| Fishbone Diagram        | Complex, recurring issues                      |
| PDCA Cycle              | Implementing fixes and improvements            |
| Root Cause Verification | Confirming suspected causes before fixing      |
| Pareto Chart            | Prioritizing which problems to tackle first    |
| Run Chart               | Tracking progress or regression over time      |
| FMEA                    | Critical systems with high risk                |
| Design of Experiments   | Tuning multiple variables or running A/B tests |

---

## Key Principle

Treat every coding issue as a process problem. Use structured thinking and data wherever possible, instead of guesswork.

---
