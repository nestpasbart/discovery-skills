---
name: discovery-plan
description: Creates a discovery plan through the intake canvas (burning question, assumptions, prioritisation, mode, hypothesis, participants and method, what to do with the outcome), in chat or from a team workshop (photo of the poster or export of a board), and helps the team decide once a study is done. Use when setting up research, writing a research plan, starting a study, processing a workshop, or deciding what to do next.
---

# discovery-plan

Turns input into `intake.md` and then `plan.md` in the study folder. The team decides; the agent prepares. This skill recruits no one, spends no money and contacts no customers or participants.

Principles (from Gothelf, Brown, Levy, Sharon, Torres, Moore and Kalbach):
- Start from a question or assumptions, not from a decision. The decision comes last.
- Make assumptions explicit and research the riskiest first.
- Decide in advance when you are right (testing) or when you are done (exploring).
- Behaviour over opinion. Look for what proves you wrong, not for confirmation.
- Evidence has a source. Only what someone supplies counts: results of a questionnaire or survey, research, interviews, observations or product data. A statement without a source is an assumption, whoever makes it, including the user, a stakeholder or an expert.
- Compare rather than ask yes or no. Turn "should we build X?" into a choice between several opportunities or ideas.
- The user and their needs come first. From the start, also think about how you will reach that user later, with sales and marketing involved where it helps, so there is no gap once the product is done.
- Time-box choice moments. If a decision can be reversed, choose now on what you know and look for evidence that you are wrong.
- Every study ends in a decision. Agree up front which decision, who decides, on what date, and what the default decision is if the evidence still doesn't decide by then. "More research" is only an outcome if it serves a new, smaller decision with its own date. This keeps teams from getting stuck in discovery.
- The job before the solution. Describe what people are trying to get done without a product, technology or method in it: a job as verb + object + clarifier, a need as direction + measure + object + clarifier.

## Language

- Respond in the language the user writes in.
- Write the study files in the language of the study: the language of the workshop, the interviews or the team. If that is unclear, use English.
- For a Dutch study, use the Dutch references in `references/nl/`; otherwise use the English ones.
- Keep quotes and sticky-note text in the language they were said or written in. Never translate them.
- Folder names stay in English, whatever the language of the study.

## Data and compliance rules

These rules take precedence over everything below.
- Never put personal data of customers or participants in `intake.md`, `plan.md` or the chat: no names, email addresses, customer numbers or account numbers. Use roles or codes (P01, P02).
- `participants/` stays out of Git. Check that `.gitignore` contains the line `studies/*/participants/*`; if not, add it and say so.
- Do not suggest external tools, panels or platforms the organisation has not approved. Write "approved test tool" or "approved panel" and list the choice under open questions.
- Recruiting existing customers goes through the organisation's official channels. State in the plan that consent and the internal privacy guidelines apply.
- Follow the organisation's data classification. If you are unsure whether something may go in the repository, ask and do not write it down.

## Step 1: Choose the route

- **Chat:** someone fills in the canvas with the agent. Go to step 2.
- **Workshop:** a photo of the poster or an export of a board has been attached as an image. Go to step 3.
- **Decision:** a study is finished or its decision date has arrived. Go to the decision route at the end.

The sections, prompts and method card are in `references/intake-canvas.md`. The workshop script is in `references/workshop-script.md`.

## Step 2: Chat route

First take what is already in the conversation, and briefly ask for the context if it is missing: which product or flow is this about (existing product, prototype, idea), and what are the time and budget? Also ask which outcome the team is working towards (a product outcome, not an output or feature) and whether there is an opportunity solution tree. If so: which target opportunity does this question belong to? And: who will need to reach this user later (sales, marketing, support), and are they involved?

Then go through the seven sections in order. Ask at most two questions at a time. Show a short summary after section 3 and after section 6. Do not fill in anything the user did not say: ask, or list it under open questions.

1. **Burning question.** What do you want to know that you do not know now? Name the type: problem, users, needs, current solution, market, desire, usability, findability, better design or drop-off. If the question fits two types, name the main one first. If the question is a solution in disguise ("do customers want feature X?"), reframe it together into the underlying problem. If it is a yes/no question about one idea, turn it into a comparison of several opportunities or ideas. If the question is about what people are trying to get done, write the job as verb + object + clarifier, with no technology or solution in it, and check its altitude: ask "why?" if it is too narrow (a step in a bigger job) and "how?" if it is too broad (an aspiration with no end).
2. **Assumptions.** What do you already believe? Keep asking until there are at least five, split between business (value, cost, channel, regulation, competition) and customers (who, why, when, what they do now). Write them as "We believe that...": what must be true, specific (what, when, how). If the question is about a solution or idea, also use the five types (desirability, viability, feasibility, usability, ethics) and find them with a story map per idea, a pre-mortem or by walking up the tree (solution → target opportunity → product outcome → business outcome). Look at what must be in place around the product too (support, onboarding, integration, partners: the whole product). Check whether there is an assumption about how you will reach the user (promise, channel, price). If not, ask whether that is deliberate. For a new product or a new group, also walk through the barriers to adoption (Jobs Atlas, via Kalbach): no understanding of the job, behaviour change, several decision-makers, high cost, high risk, unfamiliar category, missing infrastructure, new pain points, hype, wrong audience. And what keeps people with the old way: anxiety about the new and habit (the four forces).
3. **Prioritise.** Score each assumption on risk if it is wrong (high/low) and current evidence (strong/weak/none). High risk plus weak or no evidence goes through, three at most. Ask the user to confirm the selection. The evidence rule below applies.
4. **Mode.** Can the user write down what they believe is true? Yes: test. No: explore. If the data cannot exist yet (a market that does not exist yet), a small qualitative study is justified: a few sharp stories then say more than a forecast.
5. **Hypothesis or done criterion.** Test: "We believe that [assumption] for [whom]. We are right if we see [behaviour or signal] in [number]." Explore: "We are done when we can describe [...]." Record this before there is any data. Write criteria in counts, not percentages ("at least 5 of the 10"), with the number of participants, and for a sequence of actions a threshold per step. If it is about the proposition as a whole, the elevator test can be the form: for whom, dissatisfied with which alternative, different from what. If it is about a need, write it as a need statement (direction + measure + object + clarifier, for example "minimise the time it takes to ..."). Per stage, a hypothesis can carry the job (Lowdermilk and Rich): customer ("[customers] are motivated to [motivation] when doing [job]"), problem ("... are frustrated by [job] because of [problem]"), concept and feature, each with a criterion.
6. **Participants and method.** At most two segments, based on behaviour or trigger. Numbers: usability test 5 per segment, interviews 6 to 8, jobs interviews 6 to 12. In jobs-to-be-done research, recruit people who perform the job, not only existing customers, and keep brands and products out of the screener. Colleagues in sales and support are a good recruiting channel, within the official channels. Label participants in the screener with their adoption profile (enthusiast, visionary, pragmatist, conservative) and their role around the job (job performer, buyer, approver, technician; for business products also economic buyer, end user, technical buyer). A buyer cannot speak for the job performer, and an enthusiastic early user does not predict what the majority will do. Only pool findings if participants reference each other (segment check). Choose the method with the method card in `references/intake-canvas.md` and the situations below. Never ask directly about future behaviour or willingness to pay: ask about the alternative ("what would you do otherwise?") and treat price answers as a hypothesis. Combine where it is cheap, for example a screener question about the trigger in a usability test. A survey only for a concrete counting question.
7. **What do we do with the outcome?** Which decision does this study make possible, as a choice between options (A, B or stop)? Who decides, and on what date? Can the decision be reversed? What is the default decision if the evidence doesn't decide by that date? When do we stop researching (stop rule)? If no decision can be named, say honestly that the study has no purpose and suggest dropping or shrinking it. Who needs to hear it, and when? Suggest that sales and marketing hear it live rather than read it afterwards. If the team needs to choose which group or study comes next: target customer scenarios (a day before and after) with scenario scoring, first individually, then together, 1 to 5 per factor, where a very low score on one knock-out factor drops the scenario.

### Evidence rule

Evidence only counts with a source that someone supplies or that is in the repository: results of a questionnaire or survey, a research report, interview snapshots or transcripts, observations, session results, or an export of product data or analytics.

- **Ask for the source whenever someone says "we already know that".** Without a source it is not evidence: set it to `none`, however firmly it is stated and whoever states it. It stays an assumption and can go into the study.
- **Read the source yourself.** Does it really say what the assumption says? Record the source and where to find it (path, document, date) in the table. If you cannot open the source, it does not count until it is supplied.
- **Strong** is behaviour of several people from the right segment, from a source recent enough for the question. **Weak** is an opinion or wish, a single case, a different segment, a small or old study, or something second-hand ("sales often hears that..."). Say why.
- **If sources contradict each other**, list both and set the evidence to weak.
- What the agent knows itself or finds online is context, not evidence about these users. Mark it as such.
- **Scores and rankings.** A score from a survey among real job performers (importance and satisfaction per need) is evidence about needs. A team score (low/medium/high, an importance-satisfaction matrix filled in without respondents, scenario scoring without a source) is an assumption, however useful for choosing.
- **Weak evidence doesn't block a decision.** The evidence rule says how sure you are, not whether you may choose. For a reversible decision, choose on weak evidence and state the confidence.

### Situations beyond the question type

| Situation | Methods |
| --- | --- |
| Discovering opportunities, continuously | Weekly story interview about the last time, interview snapshot, opportunity solution tree |
| An assumption under an idea (from a set of three) | Generate ideas, list hidden assumptions, assumption test that simulates one moment and observes behaviour |
| Go-to-market: promise, channel, price | Message or landing-page test per variant or channel, fake door with price; behaviour, not asking |
| Which group first | Target customer scenarios with scenario scoring, then choose one beachhead segment |
| After launch | Measure the outcome itself, check gaps in the whole product, funnel matrix per step, onboarding into the job, support questions as research data |
| New product, understanding the market (Kalbach) | Jobs interviews, job map, underserved needs (team version first), value proposition, assumption test |
| Improving an existing product from the job | Jobs interviews or Switch interviews, comparing solutions per job step, job stories |
| More demand for an existing offering | Switch interviews, four forces, promise, channel and price tests |
| People drop out or cancel | Cancellation interviews (Switch in reverse), funnel matrix, onboarding into the job |
| A choice under uncertainty | Decision point up front: decision, owner, date, default decision, stop rule |

Strategy tools (disruption analysis, growth strategy matrix, broadening the market, market phases) are decision frameworks for after launch, not research methods. Don't propose them as the method of a study. A study can supply their input, for example underserved needs.

## Step 3: Workshop route

Look at the attached image and transcribe the sticky notes per section:
- The colour of a sticky note decides the column for assumptions (business or customers).
- The position on the 2x2 decides the priority.
- Copy text literally. Do not improve the wording.
- Anything illegible or ambiguous gets `[?]`. Never guess.
- A sticky note on the strong-evidence side without a source: ask for the source. Without one it moves to no evidence.
- Empty sections stay empty and go under open questions.
- If the photo shows personal data, do not copy it and say so.

Then ask in chat only about the `[?]` items and empty sections, three at a time at most.

## Step 4: intake.md

Write `studies/YYYY-MM-<slug>/intake.md` following `references/intake-template.md`.

## Step 5: plan.md

Create `plan.md` in the same folder:

```markdown
# <Study name>

Status: plan · <date> · owner: <role> · source: <workshop or chat>

## Burning question
<question> (type: <type>)

## Outcome and target opportunity
- Outcome: <product outcome, or: none>
- Target opportunity (opportunity solution tree): <opportunity, or: none>

## Riskiest assumptions
| Assumption | Column | Risk | Evidence | Source |
| --- | --- | --- | --- | --- |

## Mode
Explore / test, because ...

## Hypothesis or done criterion
- ...

## Method
<method> because <reason, linked to the question type>.
- How the results are processed: <interview snapshot, observation spreadsheet, team synthesis>
- Pitfalls to watch: ...
- Considered and not chosen: <method>, because ...

## Participants
- Segments: ...
- Number: ...
- Recruitment: approved panel / existing customers through official channels
- Adoption profile and buying role: ...
- Screener criteria: must ..., excludes ...
- Consent and privacy: according to the internal guidelines

## Planning
| Step | Date |
| --- | --- |

## Decision
- Decision (options): A ... / B ... / stop
- Who decides: <role>
- Decision date: ...
- Reversible: yes / no
- Default decision if the evidence doesn't decide: ...
- Enough evidence: <threshold from the hypothesis, or done criterion>
- Stop rule: we stop researching when ...

## What we do with the outcome
- Choices this can change: ...
- Who needs to hear it (think of sales and marketing): ...
- When: ...

## Go-to-market
- Who will need to reach this user later, and are they involved: ...
- Assumptions about promise, channel or price in this study: ... (or: deliberately not, because ...)

## Existing knowledge
- <insight> (source: <path or document, date>), or: none

## Open questions
- ...
```

Check before you finish:
- Can the outcome still change anything? If not, say so honestly and suggest dropping or shrinking the study.
- Is this research or selling? Conversations with prospects are research: no pitching.
- Do earlier studies (`studies/*/insights/`) already answer the question?
- Is it about one idea? Suggest comparing at least three ideas and testing their shared assumptions.
- Is there a decision with an owner, a decision date and a default decision? If not, add it before the plan is ready.
- Is analysis paralysis looming? Look at earlier studies and the decision log: has the same question been researched before, did an earlier study end without a decision, has a decision date moved, or does the team want more data for a reversible decision? Name it, and suggest shrinking the study or choosing now. Choose the lightest method that can carry the decision: interviews and a job map are often enough, a large survey rarely.
- Does every piece of evidence marked strong or weak have a source you have read? If not, set it to none.
- Are the files free of personal data?

Also write `status.md` with `phase: plan-ready`, the date, the decision date and the next step, and create the folders `instruments/`, `participants/`, `sessions/`, `snapshots/`, `insights/` and `readout/` if they do not exist yet.

## Finish

Summarise the plan briefly in chat and suggest having the team review it through a pull request. Do not start a next phase without agreement.

## Decision route

Use this route when a study is finished, when the decision date has arrived or passed, or when someone asks "what should we choose now?" or "do we need more research?".

1. Read `plan.md` (especially Decision and Hypothesis), `status.md` and what is in `insights/` and `snapshots/`.
2. Put the evidence per option side by side, using the evidence rule: source, strong, weak or none.
3. Compare with the threshold in the plan. Met or not met: that is the decision. Unclear: the default decision, unless the decision owner deliberately chooses otherwise.
4. If the team still wants more research: only if it serves a new, smaller decision with its own date and default. Say so honestly if it looks like postponing.
5. Record the decision in `decisions.md` at the root of the repository (create it if it doesn't exist): date, study, decision, the source it is based on, confidence (high, medium, low) and next step. No personal data. Set `phase: decided` in `status.md`.
6. The agent proposes; the decision owner decides. Record nothing as decided without their agreement.
