# Restoration Scope skills

Agent skills for nature restoration teams. They work with Claude Code, Codex, Cursor and other agents that read `SKILL.md` files.

Two kinds of skill: a generic **data quality check** for any project's data, and domain checks that add their own questions to it. The **planting records check** is the first domain check; others (cookstoves, water) can follow the same pattern.

## Data quality check

Can you trust your project's data, whatever the project: tree planting, cookstoves, water points or trainings?

Point your agent at one file or a whole project folder: activity logs, beneficiary lists, field-app exports, maps, follow-up surveys, photos, contracts. It asks what the data is for and what should exist, reads every file, and writes a report:

- how places, people, activities, follow-ups and evidence connect;
- four tests on the records: exhaustive, complete, correct, current;
- what your maps show and whether they hold up;
- example rows from your own files for each gap, every gap in `gaps.csv`, and what to fix first.

See an [example report](skills/data-quality-check/references/example-report.html), from a made-up cookstove project.

## Planting records check

Can your planting records say who planted what, exactly where and when, and how the trees are doing now?

It asks four planting questions (who planted, what, exactly where, and when), then runs the whole data quality check on the same files, with planting rules: planned, dispatched, planted and surviving trees kept apart, and survival counted against what was planted. Give it one planting log or a whole project folder.

See an [example report](skills/planting-records-check/references/example-report.html), from a made-up planting project.

It never changes your files or fills a gap with a guess, and prefers small fixes to your current workflow over new software.

## Install

```bash
npx skills add restoration-scope/skills
```

This installs both skills. Then ask something like: *"Run the planting records check on ./dawn-meadow."* or *"Run the data quality check on ./lakeside-stoves."*

## Your data

Each skill runs in whichever agent you install it in and reads only the files you point it at. It does not send anything to Restoration Scope. Your AI model provider processes what the agent reads, under your own agreement with them.

## About

Built and maintained by [Restoration Scope](https://restorationscope.com/?utm_source=github&utm_medium=referral&utm_campaign=data-diagnostic-skill), which builds digital infrastructure for nature projects: field data, maps and reporting for project teams. See how Restoration Scope works with [reforestation teams](https://restorationscope.com/solutions/reforestation?utm_source=github&utm_medium=referral&utm_campaign=data-diagnostic-skill). Questions or ideas: open an issue.

## License

[MIT](LICENSE)
