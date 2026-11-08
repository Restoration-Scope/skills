# Restoration Scope skills

Agent skills for nature restoration teams. They work with Claude Code, Codex, Cursor and other agents that read `SKILL.md` files.

## Restoration Data Diagnostic

Can your team answer these five questions from its own data, without digging through spreadsheets?

1. How many trees were planted?
2. Which species, and how many of each?
3. Where were they planted?
4. When were they planted?
5. How are they doing now?

Point your agent at the folders where your project data lives: spreadsheets, field-app exports, GIS files, photos, contracts. It inventories every source, tries to answer each question, and writes a report:

- which questions your data answers today, and from which files;
- whether sites, people, plantings and monitoring connect through stable IDs;
- what your maps show (actual planted areas, plans or program boundaries) and whether they are valid;
- a gap register (`gaps.csv`), with the source of every gap;
- a short list of what to fix first, smallest useful change first.

It is a starting point, not a pass-or-fail test. It is told never to change your files or fill a gap with a guess, and to prefer small fixes to your current workflow over new software.

### Install

```bash
npx skills add restoration-scope/skills
```

Then ask your agent something like: *"Run the restoration data diagnostic on the 2025 planting season in ./data."*

### Your data

The skill runs in whichever agent you install it in and reads only the files you point it at. It does not send anything to Restoration Scope. Your AI model provider processes what the agent reads, under your own agreement with them.

## About

Built and maintained by [Restoration Scope](https://restorationscope.com/?utm_source=github&utm_medium=referral&utm_campaign=data-diagnostic-skill), which builds digital infrastructure for nature projects: field data, maps and reporting for project teams. See how Restoration Scope works with [reforestation teams](https://restorationscope.com/solutions/reforestation?utm_source=github&utm_medium=referral&utm_campaign=data-diagnostic-skill). Questions or ideas: open an issue.

## License

[MIT](LICENSE)
