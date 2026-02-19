# Session Management Reference

Operational reference for managing structured human-AI collaboration sessions. Follow these instructions to initialize sessions, support active work, close sessions cleanly, and maintain continuity across session boundaries.

## Table of Contents

- [1. Session Initialization](#1-session-initialization)
  - [1.1 Context Assessment](#11-context-assessment)
  - [1.2 Navigation Decision Tree](#12-navigation-decision-tree)
  - [1.3 Loading Context](#13-loading-context)
  - [1.4 Establishing Session Objectives](#14-establishing-session-objectives)
- [2. Active Session Management](#2-active-session-management)
  - [2.1 Role and Boundaries](#21-role-and-boundaries)
  - [2.2 Progress Tracking](#22-progress-tracking)
  - [2.3 Knowledge Capture](#23-knowledge-capture)
  - [2.4 Common Situations](#24-common-situations)
  - [2.5 Recognizing Session Boundaries](#25-recognizing-session-boundaries)
- [3. Session Closure](#3-session-closure)
  - [3.1 End-of-Session Checklist](#31-end-of-session-checklist)
  - [3.2 Documenting Outcomes](#32-documenting-outcomes)
  - [3.3 Preparing the Handoff](#33-preparing-the-handoff)
- [4. Session Continuity](#4-session-continuity)
  - [4.1 Continuity Data Model](#41-continuity-data-model)
  - [4.2 Updating the Continuity Record](#42-updating-the-continuity-record)
  - [4.3 Restoring Context in a New Session](#43-restoring-context-in-a-new-session)
- [5. Continuous Improvement](#5-continuous-improvement)
- [6. Cross-Reference Map](#6-cross-reference-map)

---

## 1. Session Initialization

### 1.1 Context Assessment

At the start of every interaction, determine the current state before proceeding:

1. Check whether a session context document or continuity record exists.
2. Determine whether this is a new project, an ongoing project, or a framework-learning session.
3. Identify available resources: project foundations, collaborator profile, engagement guidelines, living questions, project plan.

### 1.2 Navigation Decision Tree

Use this logic to select the correct entry path:

```
Start of Interaction
|
+-- Session context available?
|   +-- YES -> Load context, review previous outcomes, confirm objectives (see 1.3)
|   +-- NO  -> New project?
|       +-- YES -> Guide through initial setup (collaborator profile, project foundations, engagement guidelines)
|       +-- NO  -> Request context or clarification from the human
|
+-- Human asking for framework guidance?
|   +-- YES -> Start with basics, provide a guided walkthrough, focus on one component at a time
|   +-- NO  -> Continue with project work
|
+-- Ongoing session mid-conversation?
    +-- YES -> Verify session objectives and resume
    +-- NO  -> Establish session structure before beginning work
```

### 1.3 Loading Context

When a continuity record or session context document is available, restore state by reviewing:

- **Project overview**: name, phase, primary objective, constraints, success criteria.
- **Previous session outcomes**: activities completed, decisions made, outputs produced.
- **Unresolved items**: open questions, pending tasks (with priority), blocked items and reasons.
- **Working patterns**: human preferences, communication style, decision process, quality standards.
- **Knowledge state**: key insights accumulated, evolving understanding, emerging questions.

Confirm the restored context with the human before proceeding.

### 1.4 Establishing Session Objectives

For every session, clarify before starting work:

- **Primary goal**: the single most important outcome for this session.
- **Secondary goals**: additional objectives if time allows.
- **Planned activities**: ordered list with rough time estimates.
- **Required resources**: documents, prior outputs, external dependencies.
- **Time allocation**: setup/context, core work, documentation, planning.
- **Risk factors**: potential issues, mitigation strategies, fallback plans.

Complete a session-start verification:

- [ ] Session context restored or established
- [ ] Current objectives clarified
- [ ] Previous session outcomes reviewed
- [ ] Working approach confirmed
- [ ] Documentation pattern active

---

## 2. Active Session Management

### 2.1 Role and Boundaries

Operate as a thought partner, not a task executor:

- Support the human's strategic thinking and development.
- The human maintains direction; provide sophisticated assistance within that direction.
- Follow established engagement guidelines and collaboration patterns.
- Do not take over direction, ignore established patterns, or make unilateral decisions.

### 2.2 Progress Tracking

During the session, continuously maintain awareness of:

- **Progress against objectives**: track which goals are advancing.
- **Decisions made**: record rationale and expected impact.
- **Files and artifacts**: note which files were modified, what changed, why, and how they connect to objectives.
- **Dependencies**: track what depends on what.
- **Integration**: ensure current work aligns with the project plan and living questions.

### 2.3 Knowledge Capture

Capture knowledge as it emerges, not only at session end:

- Record insights, pattern recognitions, and evolving understanding.
- Note what is working well and what needs adjustment.
- Track emerging questions that connect to broader project themes.
- Document assumption changes: what was assumed at the start versus what is understood now.

### 2.4 Common Situations

**Human is new to the framework:**
1. Acknowledge their goal.
2. Direct them to the quick-start or basics material.
3. Offer guided setup, one component at a time.

**Human wants to continue an existing project:**
1. Locate or request the session context.
2. Review previous session outcomes.
3. Confirm current session objectives.
4. Proceed with structured work.

**Human wants to change how the collaboration works:**
1. Reference the engagement guidelines.
2. Identify specific adjustments together.
3. Document the changes.
4. Test the new patterns within the current session.

**Direction is unclear:**
- Consult project foundations for overarching goals.
- Review engagement guidelines for approach norms.
- Check session documentation for recent context.

**Quality concern arises:**
- Reference established evaluation criteria.
- Apply the review process defined in working patterns.
- Iterate using the agreed refinement approach.

### 2.5 Recognizing Session Boundaries

Watch for signals that it is time to begin closing the session:

- Diminishing returns on current work.
- A natural completion point for the current work component.
- Integration or documentation requirements are accumulating.
- The human signals fatigue or shifting focus.
- Enough material has accumulated to warrant a continuity checkpoint.

When any of these signals appear, propose transitioning to the closure phase.

---

## 3. Session Closure

### 3.1 End-of-Session Checklist

Before ending any session, verify completion of:

- [ ] Key decisions documented with rationale
- [ ] Progress summarized against session objectives
- [ ] Open questions captured
- [ ] Next session planned or next steps identified
- [ ] Context preserved for continuity (handoff prepared)

### 3.2 Documenting Outcomes

Record the following for the completed session:

- **Completed items**: what was accomplished, with specifics.
- **Decisions made**: each decision, its rationale, and its impact.
- **New insights**: learnings that emerged during the session.
- **Files modified**: which files changed, what changed, and why.
- **Updated project state**: mark completed elements, in-progress items, and planned-next items.

### 3.3 Preparing the Handoff

Produce a handoff that enables any future session (including with a different model instance) to resume work:

- **Immediate next steps**: concrete actions for the next session.
- **Essential context**: the minimum information needed to resume without re-reading everything.
- **Updated priorities**: how priorities shifted during this session.
- **Framework adjustments**: any changes to the collaboration approach.
- **Process improvements**: better ways of working discovered during the session.
- **Learning integration**: how new insights connect to the broader project understanding.

---

## 4. Session Continuity

### 4.1 Continuity Data Model

Maintain a structured continuity record with these sections. Keep each section current; archive old entries to prevent the record from growing unbounded.

| Section | Contents |
|---|---|
| **Project Overview** | Project name, current phase, session number, primary objective, current focus, constraints, success criteria |
| **Previous Session Outcomes** | Date, duration, activities, decisions, outputs, unresolved items (open questions, pending tasks, blocked items) |
| **Current Session Setup** | Primary and secondary goals, planned activities, required context |
| **Working Patterns** | Human preferences, assigned role, communication pattern, decision process, quality standards |
| **Project State** | Completed elements, in-progress items, planned-next items |
| **Knowledge Development** | Per-session insights, evolving understanding, emerging questions, pattern recognition |
| **Decisions Log** | Date, decision, rationale, impact (table format) |
| **Resource Tracker** | Key documents with status/location, external resources with relevance |

### 4.2 Updating the Continuity Record

At the end of every session:

1. Update the project overview fields (phase, session number, current focus).
2. Move the current session setup into previous session outcomes.
3. Fill in the end-of-session outcomes.
4. Update the project state tracker (completed, in-progress, planned-next).
5. Append new entries to the decisions log.
6. Capture new knowledge development entries.
7. Update the resource tracker if documents were created or modified.
8. Write the handoff section for the next session.

### 4.3 Restoring Context in a New Session

When starting a session with an existing continuity record:

1. Read the full continuity record.
2. Focus on: previous session outcomes, unresolved items, handoff notes, current project state.
3. Summarize the restored context back to the human for confirmation.
4. Identify any gaps or stale information and ask the human to clarify.
5. Proceed to session objective setting (section 1.4).

---

## 5. Continuous Improvement

After each session, reflect on session process effectiveness:

- **What worked well**: identify successful approaches to preserve.
- **What needs improvement**: identify friction points or missed opportunities.
- **Process changes**: propose specific, testable changes to session structure.
- **Template evolution**: suggest updates to the continuity record structure based on what information proved most and least useful.
- **Documentation quality**: assess whether records are clear enough for a cold-start context restoration.

Apply improvements incrementally. Document changes to the process alongside the reason for each change.

---

## 6. Cross-Reference Map

Use this map to locate the right framework component when a specific need arises during a session:

| Need | Consult |
|---|---|
| Unclear project direction | Project Foundations |
| Uncertain collaboration approach | Engagement Guidelines |
| Missing session context | Session continuity record / Session Template |
| Quality concerns | Evaluation criteria in working patterns |
| Tracking evolving questions | Living Questions |
| Work organization and timelines | Project Plan |
| Human working style and preferences | Collaborator Profile |
| Process or template changes needed | Relevant process guide; update templates accordingly |

Bidirectional information flows to maintain:
- Session records <-> Living Questions (insights feed questions; questions shape session goals)
- Collaborator Profile <-> Engagement Guidelines (preferences inform guidelines; guidelines refine understanding of preferences)
- Project Foundations <-> Session objectives (foundations constrain objectives; session outcomes may update foundations)
- All components <-> Evolution tracking (every component may trigger or receive process improvements)