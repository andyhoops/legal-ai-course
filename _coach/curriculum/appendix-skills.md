# Coach Notes: Appendix — Building Claude Code Skills

## When to run this

This is an optional stretch module. Run it in one of two situations:

1. **After Week 11** — the student has a CLAUDE.md and a prompt library, and you want to show them the next tier before Portfolio month starts
2. **After Week 16 (post-course)** — as a capstone extension for a student who wants to go deeper or strengthen their portfolio

It builds directly on Week 9 (case analysis template), Week 10 (prompt library), and Week 11 (CLAUDE.md). Don't run it before Week 11 — the three-tier analogy only lands if the student has built all three layers.

Estimated session time: 75–90 minutes.

---

## How to frame it

The conceptual hook is the three-tier analogy:

> "You've already built three layers. CLAUDE.md is rules pinned to your wall — always present. Your prompt library is your reference notebook — you look it up when you need it. A skill is a power tool you pick up on demand: one command and the structured template runs immediately."

The key upgrade over a prompt library entry: **the skill knows when it's needed**. The `description` field tells Claude to auto-invoke the skill based on what the user asks — you don't have to remember to use it. This is the intellectual heart of the module.

Open the session by asking the student to articulate the difference between their prompt library and a skill *before* explaining it. Let them struggle briefly — then show them.

---

## What to watch for

**The description field is the danger zone.**

Students will often copy the example skill's description pattern without thinking carefully about what their new skill is for. The `/argue-sides` and `/spot-issues` skills have different trigger conditions — and getting them wrong means the skill fires at the wrong time, or not at all.

Push them with: *"What question would someone have to ask for Claude to auto-invoke this skill? Say it in plain English. Now does your description actually capture that?"*

If a student writes a description like `"Use this skill for legal analysis"`, both their skills will clash and neither will work well. Good descriptions are specific: *"Use when asked to consider both sides of a dispute"* is different from *"Use when asked to analyse or explain a legal case."*

**The `$ARGUMENTS` pattern can be misunderstood.**

Some students think `$ARGUMENTS` is a variable they define. Clarify: it's replaced by whatever comes after the skill name at invocation time. If they type `/argue-sides [some scenario]`, the full scenario text becomes `$ARGUMENTS`. They don't configure it — they just use it.

**Copying without understanding.**

The worked example for `/argue-sides` provides the complete SKILL.md content. Watch for students who copy it verbatim without reading it. Ask them to explain — in their own words — why the prompt body has the structure it does, and what would happen if you removed the "Worth checking" section.

---

## The `/spot-issues` task is deliberately less guided

This is intentional. By the time a student reaches this point, they should be able to design a prompt with less scaffolding. If they struggle, ask:

- "When you first look at a new scenario, what's the first question you'd ask yourself?"
- "What would a solicitor do before drafting any advice?"
- "What areas of contract law have you covered? Could the skill structure its output around those categories?"

Don't give them the answer. The thinking is the point.

---

## Portfolio angle

Skills in `.claude/skills/` are committed to the git repo and immediately usable by anyone who clones it. This is genuinely impressive:

- It demonstrates that the student understands Claude Code at a structural level, not just conversationally
- It shows evidence of iterative design (you have to test and refine skills to make them work)
- It's something a university admissions tutor or employer can actually *run*, not just read about

Encourage the student to write a short `tools/skills-readme.md` documenting each skill: what it does, why they designed it that way, and an example. This becomes a key portfolio artefact.

---

## Common questions

**"Can a skill call another skill?"**

Not directly — but you can design skills whose outputs are intended to feed into another. For example, `/spot-issues` identifies what's in play, then `/argue-sides` or `/analyse-case` goes deeper on a specific issue. Frame this as a workflow, not a technical feature.

**"Can I add more fields to the frontmatter?"**

There are advanced frontmatter options (like controlling which tools a skill can use, or whether it can be invoked by other agents). For this course, we're not covering those — they add complexity without benefit at this stage. If the student is curious, acknowledge that these exist and point them to the Claude Code documentation, but don't go down that path in this session.

**"Why does my skill not auto-invoke?"**

Usually the description doesn't match the phrasing of the student's question closely enough. Ask them to read their description aloud, then read their question aloud. Where do they diverge? Revise the description to cover the actual trigger phrases they use.
