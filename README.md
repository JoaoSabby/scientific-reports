# Scientific Reports

## Purpose

This repository provides a version-controlled collection of scientific, methodological, and technical reports in statistics, machine learning, data science, predictive modeling, and related computational disciplines.

The repository is designed to support reproducible technical communication. Each report is maintained as an independent Quarto document with its own bibliography, figures, tables, and report-specific resources when required. Shared repository-level configuration is used only for elements that are common to the complete collection.

The HTML output is intended for publication through GitHub Pages. Source documents remain available together with the rendered material so that methodological definitions, mathematical notation, references, and subsequent revisions can be audited through Git history.

## Repository structure

```text
scientific-reports/
├── _quarto.yml
├── index.qmd
├── reports/
│   ├── index.qmd
│   └── <report-slug>/
│       ├── index.qmd
│       ├── references.bib
│       ├── figures/
│       ├── tables/
│       └── report-specific resources
└── docs/
    └── rendered GitHub Pages website
```

The `reports/` directory is the canonical location for report source material. A report should remain self-contained unless a resource is demonstrably shared by multiple reports.

## Current reports

### Temporal Sampling Strategies for Binary Event Prediction

A methodological paper formalizing and comparing Single Landmark, Multiple Landmarks, and Event-Based Sampling for longitudinal binary event prediction, with particular attention to rare-event settings.

Source:

```text
reports/temporal-sampling/
```

## Authoring model

The repository is implemented as a Quarto website. Reports are written in Quarto Markdown and rendered to HTML.

The standard local workflow is:

```bash
quarto preview
```

For a complete production render:

```bash
quarto render
```

Rendered files are written to:

```text
docs/
```

This output directory is intentionally versioned because GitHub Pages can publish the site directly from the `docs/` directory of the `main` branch.

## Report organization

A new report should normally be created under:

```text
reports/<report-slug>/
```

The preferred source filename is `index.qmd`, which produces a stable directory-based URL after rendering.

Report-specific bibliographies, citation styles, figures, tables, and supplementary files should remain within the corresponding report directory whenever practical. This design limits cross-report coupling and allows an individual report to evolve without modifying unrelated reports.

## Reproducibility

A methodological or empirical report should document, when applicable:

- the scientific or technical objective;
- the statistical estimand or prediction target;
- data eligibility and temporal definitions;
- feature construction rules;
- sampling design;
- validation strategy;
- evaluation metrics;
- software and execution requirements;
- bibliographic sources;
- data availability;
- code availability;
- ethical or governance constraints.

Empirical claims should not be introduced without traceable evidence. Report source files and rendered outputs should be committed together when a publication version is updated.

## Versioning policy

Git history is the primary audit trail for changes to reports. Substantive methodological revisions should be committed separately from formatting-only changes whenever feasible.

A report that evolves into an independent software package, research project, journal submission with a substantial computational codebase, or separately governed collaborative project may be migrated to a dedicated repository. The present repository is intended primarily for reports that share a common publication and documentation framework.
