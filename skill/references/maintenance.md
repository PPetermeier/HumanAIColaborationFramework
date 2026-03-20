# Framework Component Maintenance Reference

Operational instructions for maintaining and evolving the five core framework components: Project Foundations, Collaborator Profile, Engagement Guidelines, Living Questions, and Project Plan.

## Table of Contents

- [Common Maintenance Pattern](#common-maintenance-pattern)
  - [Review Cadence](#review-cadence)
  - [Update Triggers](#update-triggers)
  - [Update Implementation](#update-implementation)
  - [Quality Checks](#quality-checks)
- [Component-Specific Guidance](#component-specific-guidance)
  - [Project Foundations](#project-foundations)
  - [Collaborator Profile](#collaborator-profile)
  - [Engagement Guidelines](#engagement-guidelines)
  - [Living Questions](#living-questions)
  - [Project Plan](#project-plan)
- [Cross-Component Integration](#cross-component-integration)

---

## Common Maintenance Pattern

All five components share a recurring maintenance cycle. Apply the following pattern uniformly, then layer on the component-specific guidance in the next section.

### Review Cadence

| Frequency | Scope |
|-----------|-------|
| **Per-session** | Note friction, emerging needs, and quick fixes. |
| **Weekly** | Evaluate effectiveness across recent sessions. Identify recurring issues. Plan adjustments. |
| **Monthly** | Assess strategic alignment, evolution trends, and documentation completeness. Perform deeper restructuring if needed. |
| **Quarterly** (Foundations only) | Deep examination of fundamental assumptions and standards. |

### Update Triggers

Initiate a review of any component when:

- The project enters a new phase or changes scope.
- Roles, responsibilities, or stakeholders change.
- New tools, methods, or workflows are introduced.
- Significant friction, quality issues, or pattern failures emerge.
- The user explicitly requests a change.

### Update Implementation

For every update to any component:

1. Record the specific change and its rationale.
2. Assess impact on other components (see [Cross-Component Integration](#cross-component-integration)).
3. Increment the version or changelog entry.
4. Validate that the updated component remains internally consistent.
5. Confirm the change with the user before finalizing.

### Quality Checks

After any update, verify that the component:

- Remains internally consistent (no contradictions).
- Preserves essential information (nothing silently dropped).
- Reflects current, actual practices (not aspirational or stale).
- Maintains clear, unambiguous language.
- Integrates correctly with dependent components.

---

## Component-Specific Guidance

### Project Foundations

**What it contains:** Core project parameters, working principles, quality standards, technical infrastructure, intellectual framework.

**Unique maintenance concerns:**

- Foundations change the least frequently but have the widest blast radius. Treat every edit as high-impact.
- Validate against three sub-domains when triggers fire:
  - *Core Framework* -- purpose, scope, key definitions, assumptions.
  - *Intellectual Framework* -- theoretical insights, methodological standards, quality criteria.
  - *Operational Structure* -- working patterns, documentation conventions, integration patterns.
- On quarterly review, reassess whether foundational assumptions still hold. Challenge them explicitly.
- When technical infrastructure changes (new tools, security requirements, performance issues), update the relevant infrastructure section and propagate to Engagement Guidelines and Session Templates.

### Collaborator Profile

**What it contains:** User working preferences, expertise areas, learning objectives, energy patterns, communication needs.

**Unique maintenance concerns:**

- Profile data is personal. Always confirm changes with the user; never infer and commit silently.
- Track growth over time: skill development, preference evolution, role transitions. Maintain a lightweight growth log.
- Watch for signals that the profile is stale: the user repeatedly corrects the same assumption, or session friction traces back to outdated preferences.
- When the user develops new skills or shifts energy patterns, update the profile and check whether Engagement Guidelines need corresponding adjustments.

### Engagement Guidelines

**What it contains:** Collaboration patterns, communication approaches, documentation standards, tool usage conventions.

**Unique maintenance concerns:**

- These are the most frequently tested component -- every session exercises them. Prioritize low-friction iteration.
- Track pattern effectiveness: which collaboration patterns work, which cause friction, which are unused.
- Maintain a short list of active "experiments" (pattern adjustments being trialed) and retire or adopt them within a few sessions.
- When refining a pattern, test the adjustment for at least one full session before committing the change to the guidelines.
- Probe the user periodically: "How are the current patterns working?" / "What challenges have emerged?"

### Living Questions

**What it contains:** Open questions, active investigations, knowledge development tracking, insights, and their evolution over time.

**Unique maintenance concerns:**

- This is the most dynamic component. Expect frequent additions and refinements.
- For each question, track: current understanding, investigation status, evidence gathered, and connections to other questions.
- Promote question lifecycle management:
  - *New* -- capture clearly, assign investigation direction.
  - *Active* -- update with findings each session.
  - *Resolved* -- document the answer and what it unlocked.
  - *Retired* -- archive questions that are no longer relevant, with rationale.
- Surface connections between questions. A finding in one investigation often informs another.
- Balance breadth (new questions) and depth (progressing existing investigations). Flag when the list grows without resolution.

### Project Plan

**What it contains:** Work organization, milestones, timelines, resource allocation, progress tracking.

**Unique maintenance concerns:**

- Anchor reviews to objective progress: compare actual state against planned milestones, not just activity.
- Track resource allocation efficiency. Flag when effort diverges significantly from plan.
- When adjusting the plan, distinguish between:
  - *Scope changes* (new work added or removed) -- require Foundations review.
  - *Timeline shifts* (same work, different schedule) -- update plan and notify user.
  - *Quality adjustments* (changing standards) -- require Foundations and Engagement Guidelines review.
- Maintain a running list of risks and blockers. Review them weekly.

---

## Cross-Component Integration

Changes in one component frequently require updates in others. Use this dependency map to identify ripple effects.

| When this changes... | Check these for impact |
|---|---|
| **Project Foundations** | All other components (widest impact). Especially Engagement Guidelines (working patterns) and Project Plan (scope/standards). |
| **Collaborator Profile** | Engagement Guidelines (communication style, energy patterns), Session Templates (session structure preferences). |
| **Engagement Guidelines** | Session Templates (operational patterns), Collaborator Profile (if guidelines reveal changed preferences). |
| **Living Questions** | Project Plan (new investigations may require time/resources), Foundations (resolved questions may shift understanding). |
| **Project Plan** | Living Questions (timeline pressure may reprioritize investigations), Foundations (scope changes). |

**Integration protocol:**

1. Before committing any component update, scan the dependency row above.
2. For each impacted component, determine whether the change requires an immediate update or a flagged review at next cycle.
3. Document cross-component updates in both the originating and receiving components.
4. When multiple components update simultaneously, verify terminology and process consistency across all changed files.