---
name: discovery-plan
description: Creates a discovery plan through the intake canvas (burning question, assumptions, prioritisation, mode, hypothesis, participants and method, what to do with the outcome), in chat or from a team workshop (photo of the poster or export of a board). Use when setting up research, writing a research plan, starting a study or processing a workshop.
---

# discovery-plan

Turns input into `intake.md` and then `plan.md` in the study folder. The team decides; the agent prepares. This skill recruits no one, spends no money and contacts no customers or participants.

Principles:
- Start from a question or assumptions, not from a decision. The decision comes last.
- Make assumptions explicit and research the riskiest first.
- Decide in advance when you are right (testing) or when you are done (exploring).
- Behaviour over opinion. Look for what proves you wrong, not for confirmation.

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

The sections, prompts and method card are in `references/intake-canvas.md`. The workshop script is in `references/workshop-script.md`.

## Step 2: Chat route

First take what is already in the conversation, and briefly ask for the context if it is missing: which product or flow is this about, and what are the time and budget?

Then go through the seven sections in order. Ask at most two questions at a time. Show a short summary after section 3 and after section 6. Do not fill in anything the user did not say: ask, or list it under open questions.

1. **Burning question.** What do you want to know that you do not know now? Name the type: need, users, current solution, workflow, desire, usability or findability. If the question is a solution in disguise ("do customers want feature X?"), reframe it together into the underlying problem.
2. **Assumptions.** What do you already believe? Keep asking until there are at least five, split between business (value, cost, channel, regulation) and customers (who, why, when, what they do now). Write them as "We believe that...".
3. **Prioritise.** Score each assumption on risk if it is wrong (high/low) and current evidence (strong/weak). High risk plus weak evidence goes through, three at most. Ask the user to confirm the selection.
4. **Mode.** Can the user write down what they believe is true? Yes: test. No: explore.
5. **Hypothesis or done criterion.** Test: "We believe that [assumption] for [whom]. We are right if we see [behaviour or signal] in [number or share]." Explore: "We are done when we can describe [...]." Record this before there is any data.
6. **Participants and method.** At most two segments, based on behaviour or trigger. Numbers: usability test 5 per segment, interviews 6 to 8. Method according to the method card. Never ask directly about future behaviour or willingness to pay: ask what people do now. A survey only for a concrete counting question.
7. **What do we do with the outcome?** Which choices can this change, who needs to hear it, and when?

## Step 3: Workshop route

Look at the attached image and transcribe the sticky notes per section:
- The colour of a sticky note decides the column for assumptions (business or customers).
- The position on the 2x2 decides the priority.
- Copy text literally. Do not improve the wording.
- Anything illegible or ambiguous gets `[?]`. Never guess.
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

## Riskiest assumptions
| Assumption | Column | Risk | Evidence |
| --- | --- | --- | --- |

## Mode
Explore / test, because ...

## Hypothesis or done criterion
- ...

## Method
<method> because <reason, linked to the question type>.

## Participants
- Segments: ...
- Number: ...
- Recruitment: approved panel / existing customers through official channels
- Screener criteria: must ..., excludes ...
- Consent and privacy: according to the internal guidelines

## Planning
| Step | Date |
| --- | --- |

## What we do with the outcome
- Choices this can change: ...
- Who needs to hear it: ...
- When: ...

## Open questions
- ...
```

Check before you finish:
- Can the outcome still change anything? If not, say so honestly and suggest dropping or shrinking the study.
- Do earlier studies (`studies/*/insights/`) already answer the question?
- Are the files free of personal data?

Also write `status.md` with `phase: plan-ready`, the date and the next step, and create the folders `instruments/`, `participants/`, `sessions/`, `snapshots/`, `insights/` and `readout/` if they do not exist yet.

## Finish

Summarise the plan briefly in chat and suggest having the team review it through a pull request. Do not start a next phase without agreement.
