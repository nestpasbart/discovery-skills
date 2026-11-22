---
name: discovery-instrument
description: Writes and checks research questions for a discovery study from plan.md - interview guide, jobs interview, Switch timeline, screener, survey, usability test script, feedback form, diary or experience sampling prompts - and reviews and rewrites questions someone brings themselves. Use when writing interview questions, a questionnaire, a screener, a survey, test tasks or a feedback form, or when asked "are my questions any good?".
---

# discovery-instrument

Turns `plan.md` into the instruments the study runs on, and makes sure every question is the right question. Can also be used on its own to review and rewrite questions from others.

The team decides; the agent prepares. This skill sends nothing, recruits no one and contacts no participants.

Principles (from Torres, Sharon, Levy, Brown, Gothelf, Moore and Kalbach):
- Every question serves an assumption or the hypothesis in the plan. A question that serves nothing goes.
- Past behaviour over opinion and future. Ask about the last time, not "usually" or "would you".
- Keep the research question (what we want to know) separate from the question to the participant (what we ask). Never ask the research question literally.
- Short. One or two story questions per interview, a survey of a few minutes, a diary entry of a few minutes.
- Neutral, in the participant's words, not the team's or the interface's.
- Ask so that the answers can count as evidence later: what someone did counts for more than what someone thinks or plans.
- Research is not selling. No pitching in a conversation; the proposition at the end at most, and then watch the reaction.
- In jobs-to-be-done research, ask about the goal and the process, never about a technology, product, brand or solution. The participant has to bring those up. See the JTBD rules below; they apply only to JTBD methods.

## Language

- Respond in the language the user writes in.
- An instrument follows the participants' language, not the team's. If the plan does not say, ask.
- Write in plain, spoken language. For a Dutch study, B1 level with "je".
- Keep questions someone brings in their own language. Translate only when asked.

## Data and compliance rules

These rules take precedence over everything below.
- Never put personal data of customers or participants in an instrument or the chat. Use roles or codes (P01, P02).
- Ask participants only what the study needs. No names, contact details or sensitive data in a screener or survey unless the approved recruiting channel requires it.
- Do not suggest external tools, panels or survey platforms the organisation has not approved. Write "approved survey tool" or "approved test tool".
- Consent and the internal privacy guidelines apply to every instrument. Put a consent line in every opening.

## Step 1: Choose the route

- **Study route:** there is a `plan.md` (phase plan-ready). Go to step 2.
- **Review route:** someone brings their own questions (pasted, as a file or as a link) without a plan, or wants an existing instrument checked. Go to Review route.
- No plan and no questions, but a research question: suggest running discovery-plan first. If the user prefers not to, briefly collect the research question, the riskiest assumptions and the audience, and continue with step 3.

## Step 2: Read the plan

Read `plan.md` and `intake.md`. Take from them:
- the burning question and its type;
- the riskiest assumptions, numbered A1, A2, A3 in the order of the plan;
- the hypothesis or done criterion, with its counts;
- the method;
- the participants: segments, screener criteria, adoption profile and buying role;
- go-to-market: assumptions about promise, channel or price.

Decide which instruments are needed:

| Method | Instruments |
| --- | --- |
| Story interview, user interviews, customer discovery | interview guide, screener |
| Jobs interview | jobs interview guide, screener, coding sheet (quote → job step, emotional or social, need, circumstance) |
| Switch interview, cancellation interview | timeline guide, screener |
| Underserved needs | importance and satisfaction survey |
| Stakeholder interviews | stakeholder guide |
| Usability test, first-click test, tree test, guerrilla test | test script, screener |
| Assumption test as a one-question survey, survey to count | survey (with screening first) |
| Experience sampling | experience sampling prompt and instructions |
| Diary study | diary instructions, entry prompts, closing interview guide |
| Feedback after use or launch | feedback form |
| Fake door, concierge MVP, A/B test, funnel analysis | no questionnaire: say this measures behaviour, and only write a screener or a short follow-up question if the plan names one |

## Step 3: Question matrix

Make the matrix first, before writing any instrument:

| Assumption or hypothesis | What must we see or hear to confirm or refute it? | Question, task or observation | Instrument |
| --- | --- | --- | --- |

- Every row starts from A1, A2, A3 or the hypothesis. Every assumption has at least one row.
- Column 2 describes behaviour or a concrete story, not an opinion. When testing, copy the threshold from the hypothesis ("at least 3 of the 5...").
- Also look for what could refute the assumption, not only for confirmation.
- Mark an assumption you cannot test with questions (do people really want this, will they pay): that needs behaviour, such as a fake door or a pre-sale. Say so and suggest adjusting the plan. Do not ask it anyway.
- If there is a go-to-market assumption, include the probe for the current alternative (below).
- For a JTBD method, column 2 describes which job step, need or circumstance you want to hear, or for Switch which force (push, pull, anxiety, habit).

Show the matrix in chat and ask for agreement. Only then write the instruments.

## Step 4: Write the instruments

Write each instrument in the order below. Give each block a time, and mark each question with the assumption it serves (A1, A2, H).

### Interview guide

1. **Opening** (2–3 min): who you are, why you are talking, how long it takes, that there are no right or wrong answers and that it is about their experience, not a product. Ask consent for recording.
2. **Context** (3–5 min): one or two questions about their situation to get them going.
3. **Story question** (the core): "Tell me about the last time you [behaviour from the assumption]." Choose the scope deliberately: narrow to improve something, broad to see alternatives and new opportunities. Say you want the long version.
4. **Probing**, no new topics: "What happened first? And then?", "What made that hard?", "How did you solve it?", "Who else was involved?" When someone says "usually", bring them back: "And that last time?"
5. **When someone asks for a feature**: "What would that do for you?" That is where the need is.
6. **Current alternative** (at the end of the story): "What do you use for this now, and what does it cost you in money, time and hassle?", "What else did you look at?", "Who do you check with before deciding?"
7. **Proposition or prototype**, only for customer discovery and only if the plan asks for it: last, and watch the reaction and follow-up questions, not politeness.
8. **Close**: "Is there anything I should have asked?", "Who else should I talk to about this?", thank them and explain what happens with their input.

At the top of the guide, not to be read out: the research question, the assumptions the conversation serves, and "write an interview snapshot straight after".

### JTBD rules

These apply only to instruments for a jobs-to-be-done method (jobs interview, Switch interview, cancellation interview, underserved needs survey, job stories), on top of the question check. For other methods, naming the product is often exactly right, as in a usability test or feedback after launch.

- **No technology, product or solution in the question.** Not "how do you use the app to track your hours?", but "how do you keep track of where your time goes?". If the participant names a tool themselves, ask what it does for them.
- **No method in the question.** Not "do you search by keyword?", but "how do you find what you need again?".
- **The job, not the purchase.** A jobs interview is about how someone reaches the goal, not how they found or chose a product. That belongs in a Switch interview or the consumption journey.
- **The right altitude.** "Why do you do that?" takes you to the outcome, "how do you do that?" to the steps. Don't get stuck in aspirations ("become a better professional") or in buttons.
- **One time, not usually.** Use the critical incident: one time it went wrong, what happened, and what should have happened.
- **No brand in the screener.** Recruit on performing the job, not on being a customer. Ask who performs the job and who buys; a buyer cannot speak for the job performer.
- **Need statements in a survey:** one need per line (no "and" or "or"), as direction + measure + object + clarifier, without technology. Never read them out in an interview; test them by talking about the job and tallying whether the theme comes up.

Extra rows for the question check (step 5), only for JTBD research:

| Problem | You recognise it by | How to rewrite |
| --- | --- | --- |
| Technology or product in a job question | "How do you use [tool] to...", product names, "the app" | The goal: "How do you make sure...", "How do you keep track of..." |
| Method or solution in the job | "Do you search by keyword?", "Do you use a spreadsheet?" | "How do you find... again?", "How do you keep an overview of...?" |
| Need and job mixed up | "How do you quickly find the cheapest flight?" | Job and needs separately: "How do you find a flight?", then probe time and price |
| Aspiration instead of job | "How do you become a better parent?" | One level down: "How do you plan...", "How do you arrange..." |
| Buying process in a jobs interview | "How did you find us?" | Keep it for a Switch interview or the consumption journey |

### Jobs interview guide

1. **Opening** (2–3 min): as in the interview guide, and say it is about their work or life, not about a product.
2. **Background** (5 min): who are you, when did you last [do the job], how did it go?
3. **The job** (10 min): what are you trying to achieve? What do you want to avoid? What else do you need to get done?
4. **The process** (20–30 min): how do you start? What comes next? How do you decide along the way? How do you know it is going well? How do you wrap up? Sketch the process together and point at steps.
5. **Needs** (10–15 min): what workarounds do you use? What do you put off or avoid, and why? What is the most annoying part? Critical incident: one time it went wrong, what happened, and what should have happened.
6. **Circumstances** (5 min): when do you do it differently? What influences your choices?
7. **Close**: as in the interview guide. Questions about the team's product only here, if at all.

At the top, not to be read out: the main job, the job performer, the hypothesis about the steps and circumstances, and "debrief straight after, fill in the coding sheet".

### Timeline guide (Switch and cancellation)

No questionnaire but the timeline as a guide, working back from the moment of switching or cancelling: using, the moment itself, actively looking, passively looking, first thought. Keep asking "what happened before that?" and "why then?". Include at least one question per force: what stopped working (push), what attracted you (pull), what you worried about (anxiety), what you had to let go of (habit). For cancelling: what stopped you getting the job done, and which outcomes stayed unmet? For business software: who decided, are they still there, what changed in your work?

### Importance and satisfaction survey

1. Screening first: does the person perform the job (behaviour, recent)?
2. For each need statement, two questions on 1–10 with labelled end points: how important is this to you, and how satisfied are you with how it goes now?
3. Randomise the order of the statements. No product or brand in the statements.
4. Keep it short enough to answer with attention; with many statements, score the steps of the job map instead. Sample: at least 150, and at least twice the number of statements; otherwise the result is a direction, not evidence. Opportunity score per need: importance + max(importance − satisfaction, 0).

### Stakeholder guide

Goals and what success looks like, earlier attempts and what was learned, constraints, what worries them, and who else is involved. Look for the problem behind the request; do not write a requirements list. Read what already exists first, so you do not ask basic questions.

### Screener

1. Turn each criterion from the plan into a question about behaviour or trigger, not demographics alone.
2. Multiple choice with distractors, so the question does not reveal what you are looking for. Do not always put the right option first.
3. A question on adoption profile: how someone adopts new solutions (first, after peers, only once it is standard, rather not). For business products, also the buying role: economic buyer, end user, technical buyer.
4. For each question: which answer qualifies and which disqualifies. Put this under the question, not in what the participant sees.
5. Eight questions at most.
6. Combine where it is cheap: one screener question about the trigger can already be data.

### Test script (usability test, first-click, tree test, guerrilla)

1. **Intro**: we are testing the product, not you; think aloud; you cannot do anything wrong; you can stop at any time.
2. **Warm-up question** about their situation, linked to the assumption.
3. **Tasks as a scenario with a goal**: "You want to [goal] for [situation]. Show me how you would do that." Do not use words from the interface and do not give away the steps.
4. For each task, not for the participant: the end point that counts as success, and the criterion from the hypothesis ("succeeds for at least 4 of the 5").
5. **After each task**: "What happened?" or "What did you expect there?", not "Was that easy?". An ease score may be added, labelled as opinion.
6. **Close**: one open question about what stood out to them.
7. Add: run a pilot with one person first, and prepare an observation spreadsheet (one row per observation, one column per participant).

Guerrilla session (about half an hour): check screener answers (3 min), problem interview on how they do it now (10 min), then the prototype with tasks (15 min).

### Survey

1. Only for a concrete counting question from the plan. If there is none, say a survey does not fit here.
2. Screening first, then the core question or questions, then two profile questions at most. Aim for a few minutes.
3. Ask about behaviour in a fixed period: "In the past 30 days, how often did you...?", or about the last time.
4. Answer options are mutually exclusive and exhaustive, with "other, namely" and "don't know" where possible. Scales with labelled end points. Randomise option order where order steers.
5. One question per screen where possible; open questions as few as possible and not required.
6. An assumption test as a one-question survey: one question about specific past behaviour, with the success criterion set in counts beforehand.

### Feedback form

1. Short: three to five questions.
2. About what someone tried and what happened: "What did you want to do?", "Did it work?", "What stopped you?", "What did you do next?"
3. One rating question at most, with labelled end points. A recommendation question (such as NPS) asks about the future: include it only if the team asks, and label it as opinion.
4. One optional question asking whether you may contact them for a conversation; that is recruiting and falls under consent.

### Diary and experience sampling

- **Experience sampling**: one question about what someone just did or experienced, answerable in about a minute. Narrow the domain and the moment.
- **Diary**: choose per event or per time interval. Two or three prompts per entry, a few minutes of work, with a filled-in example. Close with an interview guide per participant.

## Step 5: Question check

Check every question before delivering. Use the same check in the review route.

| Problem | You recognise it by | How to rewrite |
| --- | --- | --- |
| Leading | "How useful did you find...?", "Do you agree that..." | Neutral: "How did that go?" |
| Double-barrelled | Two topics, "and" or "or" in one question | Split, or keep the most important |
| Future or hypothetical | "Would you...", "Will you...", "What if..." | Last time: "When did you last do this? Tell me." |
| Willingness to pay | "How much would you pay?" | What they use now and what it costs; test a price with behaviour |
| Opinion where behaviour is needed | "What matters to you when...?" | Story: "Tell me about the last time you chose..." |
| Generalising | "How do you usually do that?" | One moment, or a fixed period in a survey |
| Solution in disguise | "Would you like a button for X?" | The problem: "What made X hard, last time?" |
| Closed where a story is needed | Yes/no in an interview | Open: "How...", "Tell me about..." |
| Jargon or interface words | Internal names, product names, screen labels | The participant's words, or the goal instead of the label |
| Gives away the answer | Screener or task shows what is right | Distractors, or name the goal without the route |
| Too far back | "Last year..." for something everyday | A recent, concrete moment |
| Options do not work | Overlapping, not exhaustive, no way out | Mutually exclusive and exhaustive, with "other" and "don't know" |
| Serves nothing | No assumption or hypothesis in the matrix | Remove, or raise as an open question for the plan |
| Asks more than needed | Personal or sensitive data without reason | Leave out |
| Asking for the ideal solution | "What would the perfect app do for you?" | "What went wrong, and what should have happened?" |

Then check the whole:
- Does every assumption in the matrix have a question, task or observation?
- Does it fit the time? Interview: one or two story questions with probing. Survey: a few minutes.
- Is the proposition, if any, at the end?
- Can an answer also refute the assumption?

## Step 6: Deliver

If there is a study folder, write each instrument to `instruments/<instrument>.md`:

```markdown
---
study: <study name>
instrument: interview-guide | stakeholder-guide | screener | test-script | survey | feedback-form | diary | experience-sampling
version: 1
language: en | nl
method: <method>
covers: [A1, A2, H]
---

# <Instrument>: <study name>

## For the team (not to be read out)
- Research question: ...
- Assumptions: A1 ..., A2 ...
- Hypothesis or done criterion: ...
- Question matrix: <table from step 3>

## <The blocks of the instrument, with times>
```

- Keep the question matrix in the instrument, so synthesis can trace answers back to assumptions.
- Update `status.md`: `phase: instrument-ready`, the date, and `next: discovery-recruit` (or `discovery-test` if recruiting is already arranged).
- Suggest a pilot with one person or a colleague before the instrument goes to participants.
- Suggest having the team review the instruments through a pull request.

Summarise briefly in chat what is in the instruments and what you deliberately left out. Do not start recruiting without agreement.

## Review route

For questions someone brings themselves, also outside a study.

1. If missing, ask: what do you want to know (the research question), from whom, and what will you do with the outcome? Without a research question you cannot judge whether a question is needed.
2. Run every question through the question check, and for JTBD research (jobs, Switch, cancellation, need statements) also through the JTBD rules. Show the result as a table:

   | # | Original question | Problem | Rewritten |
   | --- | --- | --- | --- |

   Leave good questions as they are and say they are good. Do not polish wording that already works.
3. Name what is missing: an assumption nobody tests, a screener that gives away what you are looking for, a survey that should have been an interview, or the other way round.
4. Say so honestly when questions are the wrong tool: desire and willingness to pay are tested with behaviour, not with questions.
5. Deliver the rewritten version as a whole, in the language of the original. If it belongs to a study, put it in `instruments/` and add `source: rewritten from <name or file>` to the frontmatter.
