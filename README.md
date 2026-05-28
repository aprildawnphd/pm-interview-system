# PM Interview System

A senior PM interview prep methodology system. Question bank, leadership brand brief, prep template, operating SOP, discipline rules, schema extensions, lessons learned, and one worked example.

**Built across multiple Claude Code sessions during my 2026 job search. Published as an artifact of my non-coder AI-augmented building practice.**

---

## What this is

A methodology layer for running senior PM interview prep at the depth and parallelism that a real multi-loop job search demands. Eight artifacts that together form a system: an evergreen cross-company question bank, a leadership brand brief, a blank prep template, an operating SOP, the discipline rules that emerged from running it, the coaching-state schema additions I layered on top of the underlying AI coach, lessons learned from running the system through a real search, and a fully worked composite example.

I built and ran this through a 2026 search that involved 9 concurrent interview loops across PE-backed B2B platforms, AI-product growth-stage SaaS, regulated compliance, health-data, ed-tech, audience research, and mission-driven clean energy. The methodology evolved during the search. The artifacts here are the version that emerged.

---

## What's in this repo

| File | Purpose |
|---|---|
| [`PREP_METHODOLOGY.md`](PREP_METHODOLOGY.md) | The operating SOP. Workflow, principles, verification discipline. |
| [`Interview_Question_Bank.md`](Interview_Question_Bank.md) | Cross-company evergreen question bank. Refined canonical answers organized by question type with audience variants. |
| [`Leadership_Brand_Brief.md`](Leadership_Brand_Brief.md) | Brand-organized leadership artifact. Identity statement, integrated principles, earned secrets, deployable signature lines, audience adaptation, 30/90-sec deployable versions. |
| [`Interview_Prep_Template.md`](Interview_Prep_Template.md) | The blank template. Copy for every new interview track. |
| [`prep-discipline-rules.md`](prep-discipline-rules.md) | The discipline rules distilled from running the system: deploy-answers-in-full, leadership-content-explicit, deliverable formatting, prep guide structure, others. |
| [`coaching-state-extensions.md`](coaching-state-extensions.md) | Additions I made to the upstream coaching state schema, with attribution. |
| [`LESSONS_LEARNED.md`](LESSONS_LEARNED.md) | Earned wisdom from running this through a real multi-loop search. May help other senior PM job seekers. |
| [`examples/example-prep-doc.md`](examples/example-prep-doc.md) | One fully worked composite example showing the methodology in practice. |
| [`NOTICE.md`](NOTICE.md) | Attribution, sanitization summary, portfolio context. |
| [`LICENSE`](LICENSE) | MIT. |

---

## How I built this

Built with [Claude Code](https://claude.com/claude-code), running on top of Noam Segal's [interview-coach-skill](https://github.com/noamseg/interview-coach-skill) (MIT-licensed). The methodology layer in this repo is mine. The underlying coaching engine that scored my answers, tracked my calibration, and held the session state across many loops is Noam's.

The work was iterative across the search:
- The Question Bank emerged from refactoring ~25 company-specific prep docs into a cross-company evergreen library after the third loop made it obvious I was re-deriving the same answers.
- The Leadership Brand Brief came from noticing that my leadership content was getting buried inside generic predicted-question entries instead of surfacing as differentiation.
- The discipline rules in `prep-discipline-rules.md` are each anchored to a specific failure mode I caught (or almost didn't).
- The schema extensions in `coaching-state-extensions.md` came from running Noam's system at scale and noticing slots that wanted to exist.
- The Lessons Learned doc is the wisdom I'm carrying forward and offering to anyone running a similar search.

Each artifact was sanitized for public release: all third-party personal names removed, all target companies anonymized to exemplar descriptors, all source-company facts about my actual employment history kept specific. See `NOTICE.md` for the full sanitization summary.

---

## Pairs with

[noamseg/interview-coach-skill](https://github.com/noamseg/interview-coach-skill) — Noam Segal's Claude Code-based interview coach. MIT License. The underlying engine.

This repo is the methodology layer. Not a fork. None of Noam's code is included here. `coaching-state-extensions.md` documents the additions I made to the upstream coaching state schema and cites Noam's upstream as the base.

---

## How to use this (if you're another senior PM)

These are my voice, my methodology, my discipline rules. They will not plug-and-play into your search. They will sketch what an AI-augmented prep practice can look like at the senior level when you take it seriously.

Useful starting points:
- Read `LESSONS_LEARNED.md` first if you're considering whether to build something similar
- Read `PREP_METHODOLOGY.md` if you want the workflow shape
- Read `prep-discipline-rules.md` for the rules that emerged
- Read `examples/example-prep-doc.md` to see what an artifact looks like end-to-end
- Read `Leadership_Brand_Brief.md` as a model for building your own
- Adapt the `Interview_Prep_Template.md` to your own structure preferences
- Build your own version of `Interview_Question_Bank.md` from your own loops

The system is not the artifacts. The system is the discipline of building and refining the artifacts across a real search.

---

## Portfolio context

This is one of several artifacts I am publishing as part of my non-coder AI-augmented building practice:

- [koudou](https://github.com/aprildawnphd/koudou) — a job-search CRM built from scratch
- [gitbent](https://github.com/aprildawnphd/gitbent) — a community brand for non-expert AI builders
- Cascading Context System — a multi-agent architecture project
- **pm-interview-system** (this repo)

The portfolio shares a thesis: senior product leaders can build credible artifacts using AI without writing the code themselves. The discipline of building this system through a real search is one form of that thesis in practice.

---

## License

MIT. See [LICENSE](LICENSE). See [NOTICE.md](NOTICE.md) for attribution.

---

*Built 2026 by [April Dawn](https://github.com/aprildawnphd) (with [Claude Code](https://claude.com/claude-code), running on [Noam Segal's interview-coach-skill](https://github.com/noamseg/interview-coach-skill)).*
