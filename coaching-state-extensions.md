# Coaching State Extensions

## Attribution

The base `coaching_state.md` schema this document extends was authored by Noam Segal as part of his open-source `interview-coach-skill` project, MIT-licensed at https://github.com/noamseg/interview-coach-skill. The canonical schema definition lives in that repo's [SKILL.md](https://github.com/noamseg/interview-coach-skill/blob/main/SKILL.md) under `## Session State System`. Every section name I use (Profile, Storybank, Score History, Calibration State, Interview Loops, etc.) is Noam's.

This document covers what I added on top while running the methodology against an active multi-loop search. None of the additions were upstreamed; on review, the upstream contribution norms did not warrant a PR for what are workflow conventions tuned to one candidate's use. They are published here as an artifact for other forkers.

## What's in the base schema (upstream)

For the canonical definition, read Noam's [SKILL.md](https://github.com/noamseg/interview-coach-skill/blob/main/SKILL.md). The base schema covers Profile, Resume Analysis, Storybank, Score History, Outcome Log, Interview Intelligence (Question Bank, Effective / Ineffective Patterns, Recruiter Feedback, Company Patterns), Drill Progression, Interview Loops, Active Coaching Strategy, Calibration State, LinkedIn Analysis, Resume Optimization, Positioning Statement, Outreach Strategy, JD Analysis, Presentation Prep, Comp Strategy, Meta-Check Log, Session Log, and Coaching Notes, plus the state-update triggers, archival thresholds, and schema migration check. All of that is Noam's, unchanged.

## What I added

Each extension below is a slot I introduced (or a convention I layered on an existing slot) while running the system. Format: rule + rationale + usage.

### 1. Operating Philosophy & Frameworks slot

A net-new top-level section between Profile and Resume Analysis. Holds my stable PM operating tenets, the AI-era evolution of PM practice as I see it, the earned secret on team development (clarity + exposure + honest feedback, with exposure named as the rarest), and artifacts of the philosophy in practice (e.g., the institutional PM Network I founded at Clarivate).

Rationale: the base schema captures stories (Storybank) and positioning (Positioning Statement) but has no slot for the substrate underneath both. When an interviewer asks "what is your product philosophy," the answer is a philosophy that stories illustrate, not a STAR story. Without a dedicated slot, it kept getting re-derived from stories instead of treated as a first-class input.

Usage: pulled when mapping stories to earned secrets, when building pitches, and when sharpening language for specific interviewer lenses (a CTO probing player-coach posture gets the maturity-calibrated, hands-on coaching tenet; a CFO probing commercial discipline gets the "PM is the business leader of their product" tenet).

### 2. Calibration State graduation pattern

The base schema defines a Calibration Status field with four values (uncalibrated, calibrating, calibrated, miscalibrated) but leaves the promotion logic implicit. I made it explicit and added a refinement about what calibration actually measures.

The rule: status promotes from "calibrating" to "calibrated" after 6 consecutive post-round self-reads that match coach reads at the round level. The status note carries the streak count and anchor dates.

The refinement that emerged on the 7th read: candidate and coach reads can occupy different dimensions and both still be calibrated. In one recent screen I read the round at "potentially good fit, not sure" (fit-axis) while the coach scored 4.15 Strong Hire-leaning (performance-axis). Both accurate, just measuring different things. The rule going forward: before treating a divergence as a calibration break, check whether the candidate and coach are evaluating the same dimension.

Rationale: without a published threshold, "calibrating" persists indefinitely and "calibrated" never gets earned; without the dimension-distinction refinement, a legitimate fit-vs-performance split looks like miscalibration. Usage: once "calibrated," the coach treats at-the-round self-reads as data-equivalent to coach scoring. Pre-round catastrophizing stays tracked separately.

### 3. Question Bank to Leadership Brand Brief cross-reference convention

A workflow convention, not a schema field. The Interview Intelligence Question Bank lives in `coaching_state.md` (Noam's slot); the Leadership Brand Brief is a companion document I maintain in the same projects folder. At the top of each, a Companion callout points to the other, names the relationship, and states the rule: scan at session start, update at session close.

Rationale: the Question Bank is a database of asked questions with scores. The Brand Brief is the curated set of earned secrets, spiky POVs, and locked positioning lines I want firing in answers. Different artifacts, different update cadences, shared substrate. Without a cross-reference convention, I lost track of which document owned which insight and re-derived material that already existed.

Usage: when an earned secret is confirmed across 3+ rounds (the same threshold upstream uses for Effective Pattern promotion), it graduates from the Question Bank's pattern log into a Brand Brief entry.

### 4. Round Outcome in-doc capture pattern

The base schema captures post-round data in coaching_state (Outcome Log, Score History, Question Bank, Recruiter Feedback, Company Patterns). That is the aggregate view. I added a per-round Round Outcome section directly inside each round's prep doc (which lives in `Projects/active/[Company]/`, not in coaching_state). It captures same-day: 5-dimension score, hire signal, what landed, what missed, my at-the-round self-read reconciled against the coach read (the calibration data point lives here before it rolls up), and thank-you / follow-up status.

Rationale: coaching_state is the aggregate view; a prep doc is the round view. When I open a prep doc six weeks later I want the outcome visible in the same artifact I prepped from. Filling Round Outcome same-day also forces the debrief inside a 4-hour window, before exact phrasing has decayed.

Usage: every per-round prep doc carries a Round Outcome placeholder pre-round, filled same-day post-round, referenced from the coaching_state Interview Loops entry. Aggregate fields stay authoritative for cross-loop pattern detection; the per-doc Round Outcome stays authoritative for round-level context.

### 5. Story Details enhancements beyond standard STAR

The base Story Details schema defines Situation, Task, Action, Result, Earned Secret, Deploy for, and Version history. I extended individual stories with three fields as they earned them:

- **Multi-chapter Action and Result.** For meta-stories spanning multiple time periods on the same thesis (one story with an AI/ML chapter in 2021-22 and a GenAI chapter in 2024-25; another with 4 parallel growth levers), Action and Result are subdivided into chapters with their own headers.
- **Story arc target.** A timing line for stories with a specific delivery target ("2:20 to 2:30 in delivery"). Forces rehearsal-aloud discipline that catches over-length before the round.
- **Backup / secondary example.** A second person or incident named with its trigger ("Deploy only if interviewer asks for a second person example") and its risk if deployed. Keeps the secondary option in working memory without polluting the primary.

Rationale: base STAR works for single-arc stories. It under-serves meta-stories (where the value is the through-line across instances) and stories with deployment timing constraints. The backup field exists because some questions hit twice in the same round and the second response should not improvise. Usage: added per-story as the story earns the structure; most stories use the base schema unchanged.

## How these extensions work with the upstream

These extensions layer on top of Noam's schema. They do not replace anything, do not rename anything, and do not change the upstream state-update triggers or archival thresholds. They add state that emerged from running the system across many concurrent loops, where friction showed up at the seams (philosophy under stories, calibration as a status with no published threshold, the gap between aggregate coaching_state and per-round prep docs, meta-stories that did not fit single-arc STAR).

Published here as an artifact of one candidate's live use, not as an upstream PR. Other forkers may layer different conventions; this document is meant to make mine legible, not canonical.
