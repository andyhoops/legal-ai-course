# Appendix: Building Claude Code Skills

*Stretch module — do this after Week 11 or after completing the full course.*

---

## What is a Skill?

By this point you've built three layers of your AI toolkit:

| Layer | What it is | When it's active |
|-------|-----------|-----------------|
| **CLAUDE.md** | Rules pinned to your wall | Always — every conversation in the project |
| **Prompt library** | Your reference notebook | When you look it up and paste it in |
| **Skill** | A power tool you can pick up on demand | When you invoke it with `/skill-name` |

A skill is a saved prompt that lives in your project repo and can be called like a command. Instead of hunting through your prompt library, copying text, and pasting it into a conversation, you type `/analyse-case Carlill v Carbolic Smoke Ball Co` and Claude runs the structured template immediately.

There are two ways a skill activates:

1. **You invoke it directly** — type `/skill-name` followed by any arguments
2. **Claude recognises it's needed** — the `description` field tells Claude when to auto-trigger the skill based on what you've asked

That second point is the key idea. A skill isn't just a shortcut — it's an instruction to Claude about *when this tool is appropriate*. Writing a good description is the intellectual work.

---

## Anatomy of a Skill

Skills live in a specific folder structure inside your project:

```
.claude/
  skills/
    analyse-case/
      SKILL.md
    argue-sides/
      SKILL.md
    spot-issues/
      SKILL.md
```

Each `SKILL.md` has two parts: a frontmatter block (between the `---` markers) and the prompt body.

```
---
name: analyse-case
description: Produce a structured IRAC analysis of a UK contract law case. Use when asked to analyse, explain, or summarise a legal case.
---

[Your prompt goes here, with $ARGUMENTS where you want the user's input to appear]
```

### The three things you need to understand

**`name`** — this is what you type after the `/`. The skill above is invoked as `/analyse-case`.

**`description`** — this is the intelligence of the skill. Claude reads it to decide whether to auto-invoke the skill when you ask a question. If your description is vague or wrong, the skill will fire at the wrong times — or never. Write it as a clear instruction: *what does this skill do, and when should it be used?*

**`$ARGUMENTS`** — a placeholder for whatever you type after the skill name. If you type `/analyse-case Carlill v Carbolic Smoke Ball Co`, then `$ARGUMENTS` becomes `Carlill v Carbolic Smoke Ball Co`. You can use it anywhere in your prompt body.

---

## Try your example skill

Your repo already contains a working skill: `/analyse-case`. It's at `.claude/skills/analyse-case/SKILL.md`. Open it and read it before going any further — notice how the description and the prompt body connect.

**Exercise 1 — invoke the skill directly:**

In Claude Code, type:
```
/analyse-case Carlill v Carbolic Smoke Ball Co [1893] 1 QB 256
```

Read the output. Does the structure match the IRAC template in the skill file?

**Exercise 2 — compare with a freeform request:**

Now ask the same thing without the skill:
```
Tell me about Carlill v Carbolic Smoke Ball Co
```

What's different? What does the structured skill give you that the freeform request doesn't? Write a few sentences in your journal.

**Exercise 3 — look at the description field:**

Try asking:
```
Can you explain the Carlill case?
```

Did Claude auto-invoke the skill, or did it answer freeform? This depends on how closely your question matches the description. Experiment with different phrasings and notice when the skill fires automatically.

---

## Build `/argue-sides`

Now you'll create a second skill from scratch.

**What this skill does:** Given a contract law scenario or case, it presents the strongest argument for each side — claimant and defendant — before offering any conclusion.

**Why it's useful:** It's easy to anchor on one interpretation of a case. Forcing yourself to hear both sides before deciding is a core legal skill. A skill that always does this automatically saves you from forgetting.

**Step 1 — create the folder and file:**

Create this file: `.claude/skills/argue-sides/SKILL.md`

**Step 2 — write the frontmatter:**

Think about the description carefully before writing it. Ask yourself:
- What kinds of questions should trigger this skill?
- Should it fire when someone asks "who would win?" or "what arguments could be made?"
- How is it different from `/analyse-case`?

Here is the complete `SKILL.md` to write:

```
---
name: argue-sides
description: Present the strongest argument for each side in a UK contract law dispute. Use when asked to consider both sides, identify arguments, or assess who might win a case.
---

Present the strongest legal argument for each side in the following dispute or case: $ARGUMENTS

**The claimant's case:**
What is the best argument available to the person bringing the claim? Cite any relevant cases or statutory provisions that support this position.

**The defendant's case:**
What is the best argument available to the person defending the claim? Cite any relevant cases or statutory provisions that support this position.

**The harder question:**
Which argument is stronger, and why? What would a court need to decide to resolve this?

**Worth checking:** Flag any legal point here that deserves independent verification before relying on it.
```

**Step 3 — test it:**

```
/argue-sides A shop displays a jacket priced at £50. A customer tries to pay £50 but the shopkeeper refuses, saying the price tag was a mistake.
```

Does the output give you genuinely distinct arguments for each side? If one side's argument feels thin, the prompt body may need adjusting — try it.

**Step 4 — refine the description:**

Ask Claude: "What would trigger my `/argue-sides` skill?" If the answer surprises you, rewrite the description until it accurately captures when you'd want this skill to fire.

---

## Build `/spot-issues` (less guided)

This one is more open-ended. You'll design it yourself with less hand-holding.

**What this skill should do:** Given a contract law scenario (a set of facts), it identifies the potential legal issues — what areas of law might be relevant, what questions a lawyer would ask, what problems might arise.

**Why it's useful:** In legal analysis, *issue-spotting* comes before everything else. If you miss the issue, the analysis is worthless. A skill that systematically surfaces issues is the first step in any serious analysis.

**Your task:**

Design the prompt body yourself. Think about:
- What structure would be most useful? (A list? Categories by area of law? A set of questions?)
- What should Claude flag that it might otherwise skip?
- How should it handle uncertainty — scenarios where an issue *might* exist but you'd need more facts?

**Suggested structure for your SKILL.md:**

```
---
name: spot-issues
description: [Write your own — what does this skill do, and when should it fire?]
---

[Write your own prompt body, using $ARGUMENTS for the scenario]
```

Test it with a scenario like:
```
/spot-issues Alice emails Bob offering to sell her car for £3,000. Bob replies "I'll take it for £2,500." Alice ignores him. Three days later, Bob emails saying "Fine, I'll pay £3,000." Alice has already sold the car to someone else. Bob wants to sue.
```

Does the output identify the key issues? (You should spot: counter-offer as rejection of original offer, whether a new acceptance is possible, and possibly remedies.) If it misses something, revise the prompt.

---

## Portfolio angle

Skills committed to your `.claude/skills/` folder are part of your repo. Anyone who clones your portfolio can use them immediately — they're not just notes, they're working tools.

For your portfolio, document each skill you've built:

1. **What it does** — one sentence
2. **Why you designed it that way** — what problem were you solving? What did you try first that didn't work?
3. **An example invocation and output** — show it working

You can add this to a `tools/skills-readme.md` file, or incorporate it into your main README.

The story you're telling: *I didn't just use AI — I built tools with it, thought carefully about when and how to use them, and left something useful behind for anyone who follows.*

---

## Journal prompt

Before you close this session, write a journal entry covering:

1. What's the difference between a skill and a saved prompt? Try to explain it in your own words, as if to someone who has never used Claude Code.
2. Why does the `description` field matter so much? What happens if you write a bad one?
3. Which of the three skills you've built feels most useful to you, and why?
4. If you were going to build a fourth skill, what would it do? Write the description field for it, even if you don't build the full skill yet.
