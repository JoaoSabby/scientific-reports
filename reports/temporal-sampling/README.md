# Temporal Sampling Strategies for Binary Event Prediction

## Scope

This directory contains the source material for a methodological paper on temporal sampling strategies for longitudinal binary event prediction.

The paper formalizes and compares three designs:

- Single Landmark;
- Multiple Landmarks;
- Event-Based Sampling.

The analysis emphasizes the distinction between feature construction, prediction horizon definition, landmark selection, temporal sampling, repeated observations per individual, and event-oriented sampling. Rare-event prediction is used as the principal methodological motivation.

## Files

- `index.qmd`: primary Quarto manuscript.
- `references.bib`: scientific bibliography in BibTeX format.
- `nature.csl`: Nature-derived CSL style with citation locator support for HTML rendering.
- `nature-html.css`: report-specific scientific HTML styling.

## Rendering

The report is part of the repository-level Quarto website. From the repository root, execute:

```bash
quarto preview
```

For a complete render:

```bash
quarto render
```

The generated page is written under:

```text
docs/reports/temporal-sampling/
```

## Methodological status

The manuscript provides formal definitions, mathematical notation, temporal diagrams, methodological assumptions, validation requirements, and a proposed comparative evaluation protocol. It does not report empirical superiority of one strategy because no comparative empirical experiment has been incorporated into the current version.

## Publication requirements

Before formal scientific submission or archival publication, author metadata, institutional affiliation, conflict-of-interest declarations, funding information, ethical considerations, code availability, and data availability statements should be reviewed and completed where applicable.
