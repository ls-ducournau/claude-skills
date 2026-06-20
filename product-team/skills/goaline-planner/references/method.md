# Goaline Method — Reference

Detailed reference for the goaline planning method, validated on two phases (Phase 0: Fondations, Phase 1: POC technique).

---

## Two-Layer System

### Layer 1: Cartographie (Reserve)
- Atemporal — doesn't change when phases are filled
- Pattern-level — captures what any company needs, not project-specific data
- Organized by chantiers (workstreams), grouped under fundamental functions
- Activities are verbs of action, not deliverables or status markers

### Layer 2: Phases (Containers)
- Filled by picking activities from the cartography
- Each phase has an objective that defines what enters it
- Resources + context determine which activities are feasible
- Phases are goalines (horizons), not milestones on a rail

---

## The Selection Process

### Step 1: Chantier Activation (Pass 1)
Fast pass — for each chantier, ask: "Does this chantier have ANY work to do in this phase?"

Justify with a short reason (one sentence). This eliminates most chantiers quickly.

### Step 2: Activity Filtering (Pass 2)
For each active chantier, take every activity from the cartography and run it through the 4 criteria funnel.

**The funnel:**
```
Activity
  │
  ▼
[1. Serves phase objective?] ──No──→ Reserve
  │ Yes
  ▼
[2. Dependencies unlocked?] ──No──→ Reserve
  │ Yes
  ▼
[3. Feasible with resources?] ──No──→ Reserve
  │ Yes
  ▼
[4. Urgency?] ──No──→ Reserve (can wait)
  │ Yes
  ▼
ENTERS THE PHASE
```

Stop at the first "No" — no need to check remaining criteria.

### Step 3: Detailing
For each selected activity:
- **Sub-activities**: what concretely needs to be done
- **Deliverable**: what the activity produces (tangible output)

Format: table with 3 columns (Activity | Sub-activities | Deliverable).

### Step 4: Tooling Map
For each selected activity, identify which skills and agents from the catalog can assist execution. The mapping lives in the chantier files (atemporal), not in the phase files.

- Check the chantier file for existing mappings
- If no mapping exists, scan the skill catalog by domain
- Prefer specific skills over generic ones
- Include both skills (how) and agents (who thinks)

### Step 5: Ordering
Map three structures:
- **Dependencies** (A → B): one activity's output is another's input
- **Feedback loops** (A ↔ B): two activities refine each other iteratively
- **Immediate start**: activities with no dependencies from the current phase

This produces a web, not a sequence. Activities within a "tour" can be worked on in parallel. When a dependency is unlocked, the next activity can start — no need to wait for the entire "tour" to finish.

### Step 6: Challenge
After filling the phase, identify and discuss:
- Activities that barely pass the filters
- Missing activities that might have been overlooked
- Scope concerns (too many activities = unfocused phase)
- Implicit assumptions that need validation

---

## Criterion 1 Adaptation

The first criterion reformulates for each phase based on its objective:

| Phase Type | Criterion 1 becomes |
|---|---|
| Specification | "Produces a specification or decision, not execution" |
| Technical proof (POC) | "Serves to prove the technical thesis" |
| Product delivery (MVP) | "Delivers a usable product to real users" |
| Product-market fit | "Proves the market wants what we build" |
| Scale | "Accelerates the machine" |
| Expansion | "Opens new markets or segments" |
| IPO preparation | "Prepares for public market readiness" |

Criteria 2-4 remain stable.

---

## Anti-Patterns

| Anti-pattern | Why it fails | Fix |
|---|---|---|
| Linear sequencing (Tour 1 → Tour 2 → Tour 3) | Imposes artificial order. Real work is a web. | Use dependency maps + feedback loops instead |
| Project data in cartography | The cartography is pattern-level. Project data makes it brittle. | Keep project data in phase files only |
| Status markers in cartography | The cartography captures what needs to be done, not what has been done | Track progress in phase files or separate tracking |
| Filling phases without justification | Activities enter without being filtered. Scope creep. | Apply the 4 criteria explicitly |
| Over-detailing distant phases | Distant phases are uncertain. Detailing them creates false precision. | Detail close phases, keep distant ones light |
| Treating solo constraints as permanent | Team size changes. Don't shape the entire strategy around a temporary constraint. | Filter with current resources, but note when activities will unlock with future resources |

---

## Validated Examples

### Phase 0 — Fondations (specification phase)
- **Objective:** Specify everything before writing a line of code
- **Criterion 1:** "Produces a specification or decision, not execution"
- **Resources:** Solo + AI
- **Result:** 7 active chantiers, 20 activities
- **Key decisions:**
  - Design: principles + identity + DS foundations only (no screens — that's execution)
  - Engineering: choices only (stack, data architecture, API architecture) — no code
  - Legal: prepare future SAS, don't create it yet (auto-entrepreneur as vehicle)
  - Team: compensation & equity terms only (CTO not yet active)

### Phase 1 — POC technique (execution phase)
- **Objective:** Prove the technical thesis works
- **Criterion 1:** "Serves to prove the technical thesis"
- **Resources:** Solo + AI
- **Result:** 4 active chantiers, 11 activities
- **Key decisions:**
  - Design stays active (POC must be demonstrable to various stakeholders)
  - Real-time/triggers in scope (automation is part of the product promise)
  - Performance: basic checks only, not formal testing
  - SAS creation moved to Phase 2 (auto-entrepreneur carries Phase 0-1)
  - Finance stays in reserve (no new financial decisions needed)
