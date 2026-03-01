# Month 2 — Going Deeper
*"Thinking harder about how you ask — and what you believe"*

## What this month is about

Month 1 was about discovery. Month 2 is about rigour. You start asking harder questions, building multi-step conversations, and — crucially — learning to interrogate what Claude tells you. This is where critical thinking becomes the main skill.

By the end of Month 2 you will:
- Be comfortable with multi-turn, structured conversations with Claude
- Have developed analytical frameworks for comparing cases
- Be able to spot when Claude is hedging, oversimplifying, or potentially wrong
- Have 8 journal entries and a growing prompt library
- Have your GitHub repo set up with first commits pushed

---

## Week 5 — Terms and Conditions

**Opening question:** *Have you ever actually read a terms and conditions document? What do you think it's really for?*

### Legal content
- Express vs implied terms
- Incorporation of terms: signature, notice, course of dealing
- Exclusion clauses and the problem of the signed form
- Case anchor: ***L'Estrange v Graucob* [1934]** — the cigarette machine contract, the clause in small print, the rule that you're bound by what you sign
- Statutory control: Unfair Contract Terms Act 1977, Consumer Rights Act 2015

### AI skill: Multi-turn conversations
- Don't ask everything in one prompt — build a conversation
- Use "based on what you just said..." and "can you go further on..." to deepen the analysis
- Try to have a conversation that lasts 8–10 exchanges on a single topic, each building on the last

### Session activities
1. Start with a broad question about exclusion clauses, then systematically narrow: "now give me the rule for consumers specifically... now apply it to this scenario..."
2. Ask Claude to argue both sides of *L'Estrange v Graucob* — first for the company, then for Mrs L'Estrange
3. Ask: "If you were advising a Parliament drafting new consumer protection legislation, what would you change about the current rules on exclusion clauses?"

### Journal prompt
> "L'Estrange signed something she hadn't read and lost her legal case because of it. Is that fair? Or does it matter that she signed?"

---

## Week 6 — Breach and Remedies

**Opening question:** *If someone breaks a promise and it causes you a loss, how far should their liability go?*

### Legal content
- What constitutes a breach of contract
- Types of remedy: damages, specific performance, injunction, rescission
- The limiting principle: remoteness of damage
- Case anchor: ***Hadley v Baxendale* [1854]** — the broken mill shaft, the carrier, the rule that has governed damages for 170 years
- The two limbs of *Hadley*: losses that arise naturally, and losses in the contemplation of the parties

### AI skill: Asking follow-up questions
- A single-prompt answer is rarely enough for complex legal topics
- Practice the skill of finding the gap: what did Claude not tell you? What assumption is buried in its answer?
- Try: after any answer, always ask "what's the strongest counterargument to what you just said?"

### Session activities
1. Ask Claude to explain *Hadley v Baxendale* — then probe: "You said losses must be 'in the reasonable contemplation of the parties' — what does 'reasonable contemplation' actually mean in practice? How have courts applied it?"
2. Ask Claude to generate a modern hypothetical where the *Hadley* rule would work unfairly, then argue the other side
3. Try to construct the facts of a case where one business sues another for lost profits — would *Hadley* allow recovery?

### Journal prompt
> "The rule in *Hadley v Baxendale* is 170 years old. Does Claude think it's still fit for purpose? Do you? What's your reasoning?"

---

## Week 7 — Comparing Cases

**Opening question:** *Is it possible for two cases to both be "correct" and yet reach opposite conclusions?*

### Legal content
- The development of remoteness doctrine after *Hadley*
- ***The Achilleas* [2008]** — a ship returned late, a charter missed, massive losses; House of Lords narrows the *Hadley* rule
- The debate: does *The Achilleas* create a new test (assumption of responsibility) or just apply *Hadley* more carefully?
- Why judges disagree — and why that's a feature, not a bug, of the common law

### AI skill: Comparative prompting
- Explicitly ask Claude to compare, contrast, and synthesise
- Use structured prompts: "First explain X. Then explain Y. Then identify three key differences. Then tell me which you think is the better approach and why."
- Ask Claude to adopt a position and defend it — then challenge it

### Session activities
1. Ask Claude to compare *Hadley v Baxendale* and *The Achilleas* side by side
2. Ask: "Some commentators say *The Achilleas* has created uncertainty in commercial law. Explain that argument, and then give me the best counterargument."
3. Write a short (200-word) comparative paragraph using what Claude helped you understand — this goes in the portfolio

### Journal prompt
> "Before this session, did you think law had 'right answers'? Has your view changed? What does it mean if two senior courts can disagree about the same rule?"

---

## Week 8 — When Claude Gets It Wrong (And How to Know)

**Opening question:** *How would you know if Claude was making something up — and does it matter whether it can search the internet or not?*

### Legal content
- Revisit any topic from Weeks 1–7 where you had doubts
- AI hallucination: why language models sometimes state false things confidently, even with access to live information
- Legal accuracy and why it matters: getting a case citation wrong isn't just an embarrassment — in legal work, it can mean building an argument on nothing

### AI skill: Critical evaluation — including knowing what your AI can actually do

AI capabilities are not fixed. Different tools, and different versions of the same tool, have different abilities: some can search the web in real time, others work entirely from training data with a knowledge cutoff, and some can do both depending on how they're set up. The first step in critical evaluation is knowing which situation you're in.

Even when an AI *can* browse the web, it can still hallucinate, misrepresent what it found, or confidently cite a source that says something different from what it claims. Web access is not a cure for unreliability — it just changes the nature of the risk.

- **Find out what Claude can do in your current setup.** Ask directly: "Do you have access to the internet in this context? What is your knowledge cutoff date?" Then test whether the answer is accurate.
- **Spot hedging language.** Phrases like "it is generally understood that..." or "courts have suggested..." are signals to probe further — not accept as fact.
- **Verify legal citations through authoritative sources.** For UK law, BAILII (bailii.org) is free and authoritative. Don't rely on Claude alone to confirm that a case exists, says what Claude claims, or uses the citation Claude gives — ask Claude to explain its reasoning, then check independently.
- **If Claude has web search:** ask it to link to its source, then verify the link actually says what Claude claims.
- **If Claude doesn't have web search:** use BAILII or a legal database to verify citations independently before relying on them.
- The discipline of asking: "Are you certain about this? What would change your answer?"

### Session activities
1. Deliberately ask Claude a question where you already know the answer (from Weeks 1–7) and check whether it's right
2. Ask Claude a question about a real case but with deliberately wrong facts — see if it corrects you or goes along with you
3. Ask Claude: "What tools do you have access to in this context? Can you browse the web? What is your knowledge cutoff?" Then try to verify whether Claude's answer about its own capabilities is accurate — this is harder than it sounds.
4. Look up one case from the course on BAILII and compare what you find with what Claude told you about it

### Journal prompt
> "What did you discover about what Claude can and can't do in your setup? Did anything surprise you — either a capability you didn't expect, or a limitation you assumed wasn't there? How does this change how you'll use it going forward?"
