# Report template

Write `report.md` with these sections, in this order. Keep it as short as the findings allow: a section with nothing to say gets one line. Use tables where they help scanning. Every finding carries its source reference. File times that are all identical are copy times: say so and leave freshness to the dates inside the data.

```markdown
# Restoration data diagnostic: <project>, <date>

## Summary
Three to six bullets: what the data can already answer, the most important gaps, the first step.

## 1. Scope and limitations
Project, geography, seasons, intervention types, sources in scope, exclusions, what was sampled, the decision this serves.

## 2. Source map
| Source | Format | Contains | Size | Comes from | Period | Latest data | File modified | Update cadence | Owner | Role (authoritative / derived / duplicate / uncertain) |

## 3. The five questions
| Question | Status | Answer | Sources | Steps to assemble | Confidence |
Then one short paragraph per question for its contradictions and definitions.

## 4. Records and how they connect
The canonical set found for intervention areas, people and organizations, interventions and monitoring; their identifiers; which links hold and which break. A short text outline or diagram is enough.

## 5. Geospatial assessment
Layers, geometry types, coordinate systems, validity, plan versus actual, links to records. Which checks ran and which could not.

## 6. Traceability and quality by domain
| Domain | Stage (0-5) | Exhaustive | Complete | Correct | Current | Sourced | Evidence |

## 7. Gap register
A count per kind and the most important rows in a table (What | Where | How many | Why it matters | Confidence | Field check). Every row, in full, goes to gaps.csv.

## 8. What to improve first
Numbered, smallest useful change first where it unlocks later ones. For each: the gap it closes, effort (small / medium / large), why now.

## 9. Questions for the team
What only the team can decide or confirm: expected totals, monitoring frequency, which source is authoritative, field checks.
```

`gaps.csv` columns: `id, kind, description, source, count, why_it_matters, confidence, needs_field_check`. `source` is the file and sheet, layer, column or rows; `count` only when countable; `confidence` is that the gap is real (high, medium, low, with the reason when not high); `needs_field_check` is yes or no.
