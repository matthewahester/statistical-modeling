# statistical-modeling

Public-facing Quarto **course-materials site** for an undergraduate
**Statistical Modeling: Regression, Prediction, and Explanation** course,
assembled by Matt Hester. Sibling to the main site
[matthewhester.com](https://matthewhester.com); intended to live at
`/statistical-modeling/` under that domain.

This is **assembled undergraduate course material** — synthesized lesson
notes, hands-on R/Quarto modeling labs, and curated references. It is a
durable public resource site, **not** a record of a currently scheduled
section, and **not** an LMS.

## Status

Assembled from a course-material build (2026-06). Topic flow, notes,
labs, and resources are in place. Dates, weights, and final policies are
not sealed and are authoritative in the LMS whenever the course runs.
Treat the site as a coherent draft, not a final release.

## What this site holds

- **Notes** — the weekly instructional spine (15 weeks, five parts):
  models/data/statistical questions, visualization and the modeling
  workflow, simple linear regression, interpreting regression output,
  diagnostics and model adequacy, multiple regression and adjustment,
  confounding and explanation, categorical predictors, interactions and
  effect modification, prediction and validation, logistic regression,
  model comparison and selection, and ANOVA/regression connections.
- **Labs** — four reproducible R + Quarto labs (visualizing
  relationships, fitting multiple regression, cross-validation and
  overfitting, logistic regression in R).
- **Resources** — a notation glossary, a one-page modeling reference,
  and R/Quarto setup.

The notes are the course's **own synthesis**, grounded in (not copied
from) open sources: *ModernDive* 2nd ed. (CC BY-NC-SA 4.0) and *Beyond
Multiple Linear Regression* (CC BY-NC-SA 4.0), attributed conservatively.
All example data are synthetic with seeds set.

## What does not go in this repo

Anything private to a graded offering: answer keys, assessment items,
rubrics, point values, due dates, student data, or any directory from
the private course build (`_state/`, `assessment_shadow/`,
`source_text/`, `run_reports/`, `accessibility/`). See
[`CLAUDE.md`](CLAUDE.md) for the full list. The operational, graded side
of any live offering lives in **Blackboard (the LMS)**, which is
authoritative.

## Local development

```bash
quarto render     # build to _site/
quarto preview    # live preview
```

R chunks in the notes and labs are written as **static, non-executed**
teaching code (` ```r ` fences), so the site renders **fully with plain
`quarto render` — no R installation required**.

## Layout

```
statistical-modeling/
├── _quarto.yml              # site config, navbar, sidebar, render allow-list
├── index.qmd                # landing page (hero + overview)
├── syllabus.qmd             # public course overview
├── schedule.qmd             # week-by-week topic map
├── notes/                   # weekly instructional notes + index
├── labs/                    # reproducible R/Quarto modeling labs + index
├── resources/               # glossary, modeling reference, setup + index
├── assets/                  # hero.png + icon.png (course identity art)
├── styles.css               # course-family palette
├── CLAUDE.md                # privacy + editing rules
└── README.md                # this file
```

No CI and no deploy pipeline in this repo. The combined site is
assembled and deployed by the hub repo (`matthewhester-site`). Local
builds only here; commits are deliberate and user-driven.
