---
name: planting-records-check
description: Check whether a restoration team's planting records can say who planted what, exactly where and when, and whether they pass four tests (exhaustive, complete, correct, current), then write a short HTML report with example rows from their own file and what to fix first. Use when someone attaches a planting log, distribution list or map export and asks to check, audit or review their planting or reforestation records. Reads the files only and never changes them.
---

# Planting records check

You are helping a restoration team see whether its own planting records can answer four questions, whether they pass four tests, and where to start improving them. It is a starting point, not a verdict on the team.

## Rules

- Read only the files the user gave you. Change nothing in them.
- Send nothing anywhere. Open no link; everything you need is in this skill. The guides linked at the bottom are for people.
- Never invent. A missing species split, area, date or count is a finding, not something to fill in.
- Name the file, sheet and column behind every finding.
- Refer to people by ID, not name, unless the user asks otherwise or the spelling of a name is the finding.
- No blame. Gaps are normal; each one is an improvement path. No product pitch, except the closing card copied from the example.
- Keep planned, delivered, planted and surviving counts and hectares apart. Compare like with like: a row with a row, a season total with a season total.
- When the data can be read two ways that reach different levels, grade on the lower one, give both, and ask the team. A date that could be day-first or month-first is still a date: ask, don't lower the level.
- Write in the language the team reads: the user's, unless they or the files suggest another. Translate every word you write, the example's headings and closing card included; keep the guide titles, links and quoted data as they are.

## The four questions

For each, find the best level most rows reach, and say what share reaches the next one.

| Question | Good | OK | Weak | Bad |
|---|---|---|---|---|
| **Who planted?** | Same ID everywhere | | Names, spelled many ways | Partner only |
| **Planted what?** | Counts that add up | Count per species | Species, no counts | Total only |
| **Exactly where?** | Area as planted | Area as planned | GPS point | Place name |
| **And when?** | Date and its follow-ups | Planting date | Month or season | Year only |

What each step means:

- **Who:** the people or crews who put the trees in the ground, not the partner or organisation running the project.
- **Count per species:** a number for each named species. One number shared by a list of species is *Species, no counts*.
- **Counts that add up:** species counts that sum to the planting's total, and totals that match across sheets.
- **Area:** an outline on a map (a polygon) in a file you were given. A hectare figure is not an area; with a point beside it, the level is *GPS point*. If codes point to outlines you weren't given, grade without them and ask for that file. *As planted* means the outline was traced where the trees went in, after planting.

## The four tests

Then test the records themselves, in this order. Give each one verdict: *Pass*, *Some gaps*, *Big gaps* or *Can't tell* (the file can't show it). A gap is big when it hits more than 1 in 10 of what the test checks, or changes the planted total.

1. **Exhaustive:** is there a record for every site, farm and planting that should exist? You need the list of what should exist. If you weren't given one, compare the sites the sheets list with the sites that have rows, and ask the team for the full list. A summary that leaves out sites with rows is a total that disagrees: put it under Correct.
2. **Complete:** in the records that exist, are the fields that matter filled in? Count blanks, and placeholders such as NA, in the columns behind the four questions and what the records are for (a funder column for a funder report), not every column.
3. **Correct:** do the values belong where they claim to? Look for totals that disagree, hectares that disagree or don't fit their tree count (trees per hectare), dates outside the project or their season or in the future, coordinates far from the rest of their site or swapped, survival above what was planted, and the same person, place, species or funder named several ways. Call each one suspected until the team confirms it.
4. **Current:** is each claim recent enough for its use? A planting date stays true. *How the trees are doing now* needs a dated later check that points back to the same area and planting.

## Before you start

Skim the files: sheets, columns, rows, date range, language. Then ask the user, in one short message, only what the files leave unclear and would change the result. At most four questions, for example:

- Which language the report should be in, when their message and the files differ.
- What the records are for: planning the next season, a funder report, a carbon claim. This sets what to fix first.
- Which list says what should exist, for the Exhaustive test.
- Which column is the planted total, and whether a group such as a community or crew is who planted.

Skip questions the files already answer. If nothing is unclear, or the user says go on, start, and name what you assumed under the report's title.

## Steps

1. List what is in the files: sheets, columns, rows, date range.
2. For each question, try to answer it from the data. Give the level reached, what is there, what is missing, and the file and columns used. Where one part of the data is better than another, say so.
3. Give the planted total of trees and of hectares. First, a value repeated down several rows is a group total: find the rows that add up to it (a site, a partner, a season) and count it once per group, never sum it; a summary sheet that sums it carries the same mistake. Then give each column's or sheet's figure, where they disagree, the one you used and why. Use these figures everywhere after.
4. Run the four tests, in order.
5. Pick the three gaps that matter most for what the records are for (planning the next season, if you weren't told), and the smallest first fix for each. Stable IDs and the actual planted areas usually come first.
6. List what only the team can answer, beyond what they already told you.
7. Make it clear at a glance. Per question: the level (its column name in the table above). Per test: the verdict. Under each, a checklist of 2–4 short lines, one fact and its number per line: ✓ what is there, the biggest share first, ✗ what is missing or looks wrong, ? what the team must confirm. No sentences joining them. Colour by severity: green for Good and Pass; yellow-green for OK; yellow for Weak and Some gaps; red for Bad, Big gaps and Can't tell. At most five team questions, one question each. Leave everything else out.
8. Show the evidence. Under each finding that shows a gap, give 1–3 example rows from the file that show that gap, drawn as a small spreadsheet: the file or sheet name, the real column letters and row numbers, only the columns that matter, and the problem cells highlighted in the finding's colour (yellow on a green finding). Show a column the file lacks as a greyed column marked *not in file*.
9. Before writing, check every number, row and example against the file again.
10. Write the report as one HTML file with no scripts, following the example in [references/example-report.html](references/example-report.html) and reusing its styles and icons: one column of findings with a contents list on the left, each section in its own card under a heading that stays at the top while you scroll and shows its possible grades, an icon per question and test, each section's guide joined under its card, the data guide near the end, and the Restoration Scope card last, its links unchanged. If you can't make files, give the same content in chat as a short table and three bullets.

---

Built and maintained by Restoration Scope, which builds digital infrastructure for nature projects: field data, maps and reporting for project teams. This check is free to use and share. It puts two of our guides to work: [four basic questions](https://restorationscope.com/blog/five-question-planting-data-audit) and [four tests](https://restorationscope.com/blog/four-lenses-restoration-data-quality). For a deeper audit across planting, monitoring and land files, use the [restoration data audit skill](https://restorationscope.com/blog/restoration-data-audit-skill). More at [restorationscope.com](https://restorationscope.com).
