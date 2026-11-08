---
name: restoration-data-diagnostic
description: Check whether a tree-planting, reforestation, agroforestry or other nature restoration project's own data can answer five questions - how many trees were planted, which species, where, when, and how they are doing now - and report where the records break and what to fix first. Use when a restoration team asks for a data diagnostic, data audit or data health check, wants to know if its spreadsheets, GIS files or field-app exports can back a planting claim, or is preparing for monitoring, reporting, a funder or an audit. Reads local files only and never changes them.
---

# Restoration Data Diagnostic

Help a restoration team see what its existing data can already answer, where the record breaks, and what to improve first. This is a starting point, not a pass-or-fail test.

## The five questions

1. How many trees were planted?
2. Which species were planted, and in what quantities or proportions?
3. Where were they planted?
4. When were they planted?
5. How are they doing now?

They test whether a headline planting claim can be traced back to the operational records needed to understand it. Adapt the wording when the intervention is not tree planting (natural regeneration, assisted regeneration, mangroves, seeds, cuttings): keep the same five dimensions, which are quantity, composition, place, time and outcome.

## Rules that always apply

- **Read only.** Never modify, move, rename, merge, delete or reformat the source data. Write only into the report folder, outside the source folders: `report.md`, `gaps.csv` and any check scripts, never copied data. Scratch work stays in memory, or in a temporary location the user agrees to and you delete afterwards.
- **Stay in scope.** Inspect only the files and folders the user places in scope. Do not upload, share or send the data anywhere.
- **Never invent.** Do not infer missing footprints, species splits, dates, relationships, counts or outcomes. A gap is a finding, not something to fill in.
- **Suspected matches stay suspected.** When two values probably mean the same thing (`S001` and `S-001`, "Grevilea" and "Grevillea"), show the answer both ways or count the match with a visible flag, list it under questions for the team, and never merge it silently.
- **Source every finding.** Each conclusion names the file (and sheet, layer, column or row range) it came from. Keep facts, derived results, suspected issues and recommendations visibly separate.
- **Keep counts apart.** Planned, dispatched, delivered, planted, replaced, surviving and thriving are different numbers. Never add them together or swap one for another.
- **No unbacked percentages.** Without a reliable expected total, report what was observed and say why no percentage ([assessment-model.md](references/assessment-model.md#testing-exhaustiveness)).
- **No blame.** Restoration work is hard and data gaps are normal. Frame every gap as an improvement path.
- **No overclaiming.** A planting total is not ecological impact. Better data does not guarantee survival, certification, investment or funding.
- **No platform pitch.** Do not recommend new software just because the data lives in spreadsheets.
- **Names stay private.** In the report, refer to farmers, landowners, communities and partners by their IDs, not their names, unless the user asks otherwise. Never compare named partners.

## Workflow

Work through the steps in order; ask only where a step says to.

### 1. Agree the scope

Ask, in one message, and wait for the answer. Start the message by saying that their AI model provider processes whatever you read, under their own agreement with that provider, and that nothing is changed or sent anywhere else.

- Which project, geography, season(s) and intervention type(s) to assess.
- Which folder(s) or files are in scope, and anything to leave out.
- What decision or obligation the answer serves (internal management, a funder report, monitoring planning, an audit), and how recent an answer needs to be for it. If they don't say, use the monitoring interval in their protocol, or else state the assumption you made.
- Whether they know the expected totals: how many sites or farms are in scope, how many trees were planned, how often each site should be monitored. If they don't, that becomes a finding, not a blocker.
- Where to write the report. If they don't choose, use a new `restoration-data-diagnostic/` folder next to, not inside, the data.

Record the agreed scope, exclusions, known limitations and the provider notice at the top of the report.

### 2. Inventory before interpreting

List every source before judging any of it, filling the source map columns in [report-template.md](references/report-template.md). Keep the file's modified date apart from the latest date inside the data: a re-saved file is not fresh data. Do not assume the first or largest spreadsheet is canonical. Open every sheet and every layer; [checks.md](references/checks.md) says how to read each format.

### 3. Find the real-world spine

Identify the best available canonical set for each of:

- **Intervention areas:** the actual footprints where work happened. Distinguish landscape or program boundaries, property boundaries, planned areas, actual footprints and monitoring plots. The test: could a field visit or satellite image find the consequences of the work from this geometry?
- **People and organizations:** owners, farmers, communities, field officers, implementing partners, with their role and dates when relevant. One person may hold several properties; one property may have several people.
- **Interventions:** dated records of what happened where (activity, quantities and units, species split, who, evidence).
- **Monitoring:** later observations tied back to the same units and, where possible, the same planting or cohort.
- **Supporting evidence:** photos, contracts, tenure documents, maps and consent records, and whether file names, folders or fields tie each one to a site, person or contract.

When sources disagree on what the full set is (the map has five sites, the log seven, the plan six), use all of them together as the working set for matching, and report the disagreement as a gap.

For each, check identifiers: is there a unique, stable ID that other records reference, consistently formatted and used? A name can work for a handful of stable sites; IDs matter more as records, seasons and contributors grow. When one property holds several footprints, each footprint is its own intervention unit that references the property.

### 4. Test the five questions

For each question, actually try to assemble the answer from the data. Report:

- **Status:** answered, partly answered, or not answered, with a few words of qualifier when it differs by period or site ("answered for March, not since").
- **The answer**, if one can be given, with its time period and definitions (for example "planted, not dispatched"). A plan target from a document may serve as a denominator if you name its source and any doubt the team has about it.
- **Sources used** and the **steps it took** to get there (joins, filters, manual matching). Many steps or manual matching is itself a finding.
- **Contradictions** between sources, unresolved.
- **Confidence:** high, medium or low, with the reason.

For question 5, look for the context that makes an observation usable: where (unit ID), when, what it assessed (a planting or cohort, or for natural regeneration the monitored area or population), the method and coverage (whole site, plot, sample), the result (survival, height, condition), who recorded it, and the evidence. If the project has a monitoring protocol, its required fields take precedence. Say which are present; this is a guide, not a universal standard. Give a survival rate only when survivors and planted trees cover the same site, cohort and method; the denominator is the planted count for that cohort, never the dispatched count. Otherwise give the counts side by side and say why no rate.

### 5. Assess structure and quality

For each domain (areas, people, interventions, monitoring, evidence), give a traceability stage and the five quality dimensions, each with the evidence behind it. The model, and how to test exhaustiveness against an expected total, are in [assessment-model.md](references/assessment-model.md). Run the geospatial and correctness checks in [checks.md](references/checks.md) that fit the formats present; say which checks ran, which could not, and which need people in the field.

### 6. Build the gap register

One row per gap, with the `gaps.csv` columns in [report-template.md](references/report-template.md), filed under the one kind that fits it best: missing source sets, missing members or expected records, records missing required fields, unstable or inconsistent identifiers, disconnected records, ambiguous definitions, suspected errors, stale information.

### 7. Prioritize improvements

Recommend a short, ordered roadmap, proportional to the team's size. Weigh risk to trees, land, people or evidence; pending operational decisions; monitoring and maintenance needs; reporting, audit or funding obligations; effort and cost to fix; and foundational fixes that unlock several later ones (stable site IDs and actual footprints usually come first). Each step names the smallest change that would close the gap.

### 8. Write the report

Write `report.md` and `gaps.csv` from [report-template.md](references/report-template.md) in the agreed folder. Then, in chat, give a short summary: the five-question table, the three most important gaps (by the weighing in step 7), and the first recommended step. End with the questions that need the team's own judgment.

## When the data is very large or messy

Inventory every source, then read headers and a sample of rows to understand each table. Scan in full every table that a total, a coverage or exhaustiveness claim, or a duplicate or orphan check depends on. Anything judged from a sample is labelled "sample only" in the report, and properties a sample cannot show (completeness of the whole set, duplicates) stay "unknown". If there is no data in scope at all, say so and offer the five questions as a checklist the team can use to set up its records.
