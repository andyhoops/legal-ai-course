# Month 3 — Building Tools
*"Making your workflow work for you"*

## What this month is about

Month 3 shifts from consumer to creator. You stop just using Claude and start building reusable assets: a prompt library, case analysis templates, and your own project configuration. This is where you discover that the most effective AI users are the ones who invest in their own tools.

By the end of Month 3 you will:
- Have a personal prompt library with 10+ well-crafted, tested prompts
- Have built at least one reusable case analysis template
- Have created a CLAUDE.md for your repo
- Have explored Claude Code's project features
- Have 12 journal entries and a case study folder with 3+ entries

---

## Week 9 — Vitiating Factors: Misrepresentation

**Opening question:** *If someone sells you a car and lies about the mileage, what should happen?*

### Legal content
- What is a vitiating factor? Why does it matter?
- Misrepresentation: a false statement of fact that induces a contract
- Three types: fraudulent (*Derry v Peek* [1889]), negligent (s.2(1) Misrepresentation Act 1967), innocent
- Remedies: rescission and/or damages depending on type
- The Misrepresentation Act 1967 — why it shifted the burden

### AI skill: Building a case analysis template
- Design a reusable prompt structure for analysing a case
- Test it on a new case: give Claude the facts and ask it to apply the template
- Refine the template based on what's missing or unclear
- Save the final version to `tools/case-analysis-template.md`

### Session activities
1. Ask Claude to explain the three types of misrepresentation with an example of each
2. Work with Claude to draft a case analysis template: "What fields should a good legal case analysis always cover?"
3. Test the template by applying it to *Carlill v Carbolic Smoke Ball Co* from Month 1 — does it work?

### Journal prompt
> "You've now built your first reusable tool — the case analysis template. What decisions did you make about what to include? What did you have to leave out, and why?"

---

## Week 10 — Vitiating Factors: Mistake and Duress

**Opening question:** *If both parties to a contract are wrong about a fundamental fact, should the contract stand?*

### Legal content
- Common mistake: both parties wrong (*Bell v Lever Bros* [1932] — the golden handshake for a terminable contract)
- Mutual mistake: parties at cross-purposes (*Raffles v Wichelhaus* [1864] — the ship Peerless)
- Unilateral mistake: one party wrong, other party knows (*Shogun Finance v Hudson* [2003])
- Duress: economic duress as a developing doctrine (*Atlas Express v Kafco* [1989])

### AI skill: Writing your own prompt library
- Audit what you've asked across all sessions — what patterns emerge?
- Write 5 new prompts from scratch, each with: a name, the prompt text, when to use it, example output
- Format: a Markdown file in `prompts/` that another person could pick up and use

### Session activities
1. Ask Claude to explain *Bell v Lever Bros* — then probe: "The House of Lords said the mistake wasn't sufficiently fundamental. What would 'sufficiently fundamental' look like? Give me an example that would pass the test."
2. Draft a prompt for each of these recurring tasks: (a) explain a case, (b) argue both sides, (c) compare two cases, (d) apply a rule to new facts, (e) identify weaknesses in an argument
3. Test each prompt and refine it

### Journal prompt
> "What makes a good reusable prompt? What have you learned about the difference between a prompt that works once and one that works every time?"

---

## Week 11 — The Consumer Angle

**Opening question:** *Why do consumers get more legal protection than businesses in contract law?*

### Legal content
- The Consumer Rights Act 2015: the modern framework
- What counts as a "consumer" and a "trader"
- Unfair terms in consumer contracts: the fairness test, the grey and black lists
- Goods and services: the implied terms under the CRA
- Why business-to-business contracts are treated differently

### AI skill: Creating a CLAUDE.md for your project
- Introduce the concept of project-level AI memory
- Write your own `CLAUDE.md` for this repo — a file that tells Claude what the project is, what conventions to use, what context to carry forward
- Discuss: why does giving Claude persistent context make it more useful?

### Session activities
1. Ask Claude to compare the protections available to a consumer vs a business in a contract dispute — what are the key differences?
2. Draft your `CLAUDE.md` with Claude's help: what does Claude need to know to be maximally helpful in future sessions?
3. Ask Claude to role-play as a Trading Standards officer advising a consumer — does the CRA 2015 help them?

### Journal prompt
> "You've now built a CLAUDE.md for your own project. What did you decide to put in it? What does it feel like to 'configure' your AI partner for your own purposes?"

---

## Week 12 — A Real Research Workflow

**Opening question:** *If you were given a legal problem to solve, what would your process be from start to finish?*

### Legal content
- Your choice: revisit any topic from the course that you want to go deeper on, or tackle a new scenario involving multiple issues (e.g. a business dispute involving exclusion clauses, misrepresentation, and damages)

### AI skill: End-to-end research session
- Run a complete research workflow using everything learned so far
- Plan: identify the issues → find the relevant rules → apply to the facts → consider counterarguments → reach a conclusion
- Use your case analysis template, your prompt library, and your CLAUDE.md
- Document the workflow so it could be repeated

### Session activities
1. Agree a legal research question or scenario (you choose — pick something that genuinely interests you)
2. Work through the full research process with Claude, using the tools built in Weeks 9–11
3. Produce a structured output — a case note, a legal memo, or a comparative analysis — that goes into the portfolio

### Journal prompt
> "Describe the research workflow you followed this session. What worked well? What would you change? Could someone else follow your process to reach the same result?"
