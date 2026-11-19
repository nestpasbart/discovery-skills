# Discovery skills

Agent skills for product discovery, by [Supported by Design](https://supportedby.design). They work with GitHub Copilot (agent mode in VS Code, Copilot CLI, cloud agent), Claude and other tools that follow the [Agent Skills](https://agentskills.io) standard.

The skills are written in Dutch.

## Skills

| Skill | What it does |
| --- | --- |
| [discovery-plan](skills/discovery-plan/SKILL.md) | Turns a research question into a discovery plan through a seven-part intake canvas: burning question, assumptions, prioritisation, mode (explore or test), hypothesis, participants and method, and what to do with the outcome. Works in chat or from a photo of a team workshop. |

The approach draws on Lean UX (Gothelf and Seiden), Practical Design Discovery (Dan Brown), UX Strategy (Jaime Levy) and Validating Product Ideas (Tomer Sharon): start from a question or assumptions, test the riskiest first, decide in advance what would prove you wrong, and favour behaviour over opinion.

## Install

With GitHub CLI 2.90 or later (`gh skill` is in public preview):

```shell
gh skill preview nestpasbart/discovery-skills discovery-plan
gh skill install nestpasbart/discovery-skills discovery-plan --pin v1.0.0
```

Or copy `skills/discovery-plan/` to `.github/skills/discovery-plan/` in your repository.

Add this to your `.gitignore`, so participant data never ends up in Git:

```
studies/*/deelnemers/*
!studies/*/deelnemers/.gitkeep
```

## Built for strict environments

The skill uses no external tools or services. It keeps personal data out of every file, refers to the organisation's approved panels and test tools, and proposes a pull request for review.

---

## Nederlands

Skills voor product discovery van [Supported by Design](https://supportedby.design). `discovery-plan` maakt een onderzoeksplan via een intake-canvas met zeven vakken, in chat of vanuit een foto van een teamworkshop. Installeren kan met `gh skill install` of door `skills/discovery-plan/` naar `.github/skills/` in je repo te kopiëren.

## License

[CC BY 4.0](LICENSE): free to use and adapt, with credit to Bart Schoenmakers, Supported by Design.
