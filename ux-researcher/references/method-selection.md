# Method selection under constraints

Goal: turn a hypothesis or a fuzzy goal into the right method, scored against cost, access, and time. The most common research failure is using a method that cannot answer the question (a survey to learn "why", interviews to estimate "how many").

## Step 1. Sharpen the hypothesis

A usable hypothesis is falsifiable: it can be shown wrong by evidence. Push vague goals into this shape:

> We believe [who] [does / wants / struggles with what] because [why]. We will know we are wrong if [observable signal].

Examples:

- Weak: "Users want better onboarding."
- Sharp (EN): "We believe new users abandon onboarding at the workspace-setup step because they do not see the value yet. We are wrong if abandonment is evenly spread across steps."
- Sharp (FR): "Je crois que les nouveaux usagers abandonnent l'onboarding a l'etape de configuration parce qu'ils ne voient pas encore la valeur. Je me trompe si l'abandon est reparti uniformement entre les etapes."

If the user has no hypothesis yet, the work is generative (exploratory), not validation. Say so. Generative work uses different methods (interviews, contextual inquiry, diary studies), not confirmatory ones.

## Step 2. Classify what you need to learn

Two axes decide the method family:

- **Attitudinal vs behavioral.** What people say (attitudes, needs, perceptions) vs what they do (actions, paths, errors). Interviews and surveys capture the said; analytics, usability tests, and diary studies capture the done.
- **Qualitative vs quantitative.** "Why and how" (small n, depth) vs "how many and how much" (large n, prevalence). Qual generates and explains; quant measures and ranks.

| You need to learn... | Family |
|---|---|
| Why something happens, the mental model behind it | Qualitative, attitudinal (interviews, contextual inquiry) |
| Whether a design is usable, where it breaks | Qualitative, behavioral (usability test) |
| How widespread an attitude or behavior is | Quantitative (survey, analytics) |
| What real behavior looks like over time, in context | Behavioral (diary study, analytics, contextual inquiry) |
| How information should be organized | Card sorting, tree testing |
| Whether variant A beats variant B on a metric | A/B test (needs traffic + a clear metric) |

## Step 3. Score the method against constraints

For each candidate method, rate cost, access, and time as Low / Med / High, and note the confidence it can give on the specific hypothesis. Pick the method that clears the constraints and still answers the question. Do not silently upgrade to the ideal study the user cannot run.

| Method | What it answers | Cost | Access need | Time | Note |
|---|---|---|---|---|---|
| User interviews (5 to 8) | Why, mental models, motivations | Med | Recruit + schedule | Med | Depth, not prevalence. Saturation often by 5 to 8 per segment. |
| Contextual inquiry | Real behavior in real environment | High | On-site or screen-share in context | High | Strongest for "what actually happens". |
| Diary study | Behavior and feeling over days/weeks | Med | Committed participants | High | Captures change over time, novelty wearing off. |
| Survey | Prevalence, ranking, segmentation | Low to Med | A reachable list | Low to Med | Cannot tell you why. Needs enough responses for the cut you want. |
| Usability test, moderated (5) | Where and why a flow breaks | Med | Recruit + a prototype | Med | 5 users surface most major issues per segment. |
| Usability test, unmoderated | Same, at scale, no facilitator | Low to Med | A tool + a prototype | Low | Faster, shallower; no live probing. |
| Card sort / tree test | Information architecture fit | Low | Participants + a tool | Low | Pair: card sort to build, tree test to validate. |
| Analytics review | What is happening, at scale | Low | Existing instrumentation | Low | Free if data exists; tells what, never why. |
| A/B test | Which variant wins on a metric | Med | Live traffic + a metric | Med to High | Needs volume to reach significance. |
| Concept / fake-door test | Demand for something not built | Low to Med | A way to expose it | Low to Med | Validates interest before building. |
| Guerrilla / intercept (5 to 10) | Quick directional read | Low | A place with target users | Low | Directional only; biased sample. |

## Step 4. Constraint triage

State the dominant constraint, then the realistic move:

- **No budget:** analytics review of existing data, guerrilla interviews, unmoderated tests on a free tier, a short survey to a list you already own.
- **No time (days, not weeks):** 5 moderated sessions, or an unmoderated test, or a one-question survey. Skip recruitment agencies; use existing customers.
- **No access to real users:** proxy users with the closest matching profile, internal colleagues for a usability smoke test (label the bias clearly), or analytics and support tickets as a behavioral stand-in.
- **High-stakes decision, low evidence tolerance:** triangulate. One qual method to explain plus one quant method to size. Do not bet a roadmap on a single method.

## Common mismatches to flag

- Survey used to answer "why" -> you get rationalizations, not reasons. Use interviews.
- Interviews used to estimate "how common" -> n is too small. Use a survey or analytics.
- Asking people to predict future behavior ("would you use this?") -> weak signal. Probe past behavior or run a concept test that requires a real action.
- Usability test treated as validation of demand -> it tests usability, not whether anyone wants the thing.

## Output format for this mode

1. Restated hypothesis (sharpened, falsifiable).
2. What needs to be learned (the two-axis classification).
3. Recommended method, with the constraint scores that justify it.
4. The tradeoff being accepted, named plainly.
5. If stakes are high: the second method to triangulate with.
