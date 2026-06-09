# Bias audit

Use when the user brings their own questions. Do not silently rewrite them. Audit, flag what is wrong and why, then offer the rewrite. The point is to make the bias legible so the user learns to spot it, not just to hand back cleaner text.

## Question-level bias taxonomy

For each: what it is, a flawed example, and a fixed version (EN and FR).

**Leading** - steers toward an answer.
- Bad: "How much did you enjoy the new dashboard?"
- Fix (EN): "What was your experience with the new dashboard?"
- Fix (FR): "C'etait quoi ton experience avec le nouveau tableau de bord?"

**Loaded** - smuggles in an assumption the person has not agreed to.
- Bad: "What do you like about our fast checkout?" (assumes it is fast and liked)
- Fix (EN): "Walk me through your last checkout. How did it go?"
- Fix (FR): "Montre-moi ton dernier passage en caisse. Comment ca s'est passe?"

**Double-barreled** - two questions in one; the answer is uninterpretable.
- Bad: "Was the feature easy to find and useful?"
- Fix: split into two. "How did you find the feature?" then "Once you used it, what did it do for you?"

**Assumptive / presupposition** - presumes a behavior or fact.
- Bad: "How often do you share reports with your team?" (assumes they do)
- Fix (EN): "Do you share reports with anyone? If so, walk me through that."
- Fix (FR): "Est-ce que tu partages des rapports avec quelqu'un? Si oui, montre-moi comment."

**Social desirability** - pushes toward the flattering answer.
- Bad: "Do you read the documentation before asking for help?"
- Fix (EN): "Last time you got stuck, what did you do first?"
- Fix (FR): "La derniere fois que tu as bloque, tu as fait quoi en premier?"

**Acquiescence** - phrasing invites agreement (yes-saying).
- Bad: "Don't you think the new flow is clearer?"
- Fix: ask open. "How does the new flow compare to before, for you?"

**Hypothetical / future-prediction** - people are poor predictors of their own behavior.
- Bad: "Would you pay for this feature?"
- Fix (EN): "What have you paid for to solve this before?" or run a concept test that requires a real action.
- Fix (FR): "Qu'est-ce que tu as deja paye pour regler ca?"

**Jargon / ambiguity** - terms the participant may read differently than intended.
- Bad: "How is the platform's performance?" (speed? reliability? value?)
- Fix: name the specific thing. "When you load a report, how long does it feel like it takes?"

**Framing / anchoring** - a number or adjective in the question sets the reference point.
- Bad: "On a scale where most users rate us 9, how would you rate us?"
- Fix: remove the anchor. "How would you rate this, from 1 to 5?" with every point labeled.

**Recency / scope too wide** - "in general" answers drift to the most recent or most vivid case.
- Bad: "How do you usually feel about onboarding?"
- Fix (EN): "Think about the last product you onboarded to. How did that go?"
- Fix (FR): "Pense au dernier produit ou tu as fait l'onboarding. Comment ca s'est passe?"

## Audit procedure

1. Read each question against the taxonomy. A question can carry more than one bias.
2. For each flagged question, state the bias name, the one-line reason, and the rewrite.
3. Check the set as a whole for: order effects (sensitive items too early), missing non-answer options on scales, hypotheticals that should be incident-based, and balance (are you only asking about positives?).
4. Note questions that are fine. Do not invent problems.

## Output format for this mode

A table, one row per flagged question:

| Original question | Bias flagged | Why it skews the answer | Rewrite (EN / FR) |
|---|---|---|---|

Below the table: set-level notes (order, balance, missing options) and a count of how many questions passed clean. If the user wants, assemble the rewritten set into an interview brief via `interview-brief.md`.
