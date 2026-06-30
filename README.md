# Criticality-aware materials informatics for sustainable sodium-ion cathode prioritization: An integrated screening of computed electrode descriptors and text-mined literature evidence

This repository contains a reproducible, criticality-aware materials-informatics workflow for sodium-ion cathode prioritization.

## Scope

The workflow combines Materials Project sodium-ion electrode records, conservative criticality-aware filtering, ChemDataExtractor text-mined battery evidence, grouped cross-validation machine learning, feature-leakage auditing, and manuscript-ready figures/tables.

The study is a decision-support workflow. It does **not** experimentally validate cathodes and does **not** claim discovery of new cathode materials.

## Main counts

- Materials Project sodium-ion electrode records: 416
- Basic electrochemical screening pass: 164
- Hard-exclusion-free candidates: 112
- Conservative earth-abundant proxy candidates: 56
- Conservative candidates with exact CDE evidence: 18
- Deduplicated manuscript shortlist: 95

## Leakage-audited ML interpretation

Notebook 06 performs target-specific leakage auditing. Na-stoichiometry near-target features are removed for capacity and energy, and stability components are removed for the derived stability_worst target. The C-strict protocol is interpreted as a post-DFT decision-support protocol, not a pre-DFT discovery model.

## Repository structure

```text
notebooks/                 Reproducible notebooks 01–07
data/processed/            Main manuscript tables
data/figure_data/          CSV files used to create figures
data/supplementary/        Supplementary Tables S1–S8 and leakage audit files
figures/main_figures/      Main figures as PNG and PDF
figures/supplementary_figures/ Supplementary figures
manuscript_assets/         Captions, abstract draft, claim-control text
```

## Run order

See `RUN_ORDER.md`.

## Data availability

Processed datasets and figure-data files will be archived at:

```text
TO_BE_ADDED_AFTER_DATA_DEPOSIT
```

Materials Project source data must be accessed through the Materials Project API subject to Materials Project terms of use. ChemDataExtractor source data should be obtained from the original public database/source.

## Code availability

The code will be archived at:

```text
TO_BE_ADDED_AFTER_ZENODO_CODE_RELEASE
```

GitHub repository:

```text
TO_BE_ADDED_AFTER_GITHUB_UPLOAD
```

## License

- Code: MIT License, see `LICENSE`.
- Processed data, figure data, and manuscript-derived tables: CC BY 4.0, see `LICENSE_DATA.md`.

## How to cite

A citation DOI will be added after Zenodo release.

## Manual checks before submission

- Replace all author, affiliation, DOI, URL, and funding placeholders.
- Verify Supplementary Table S1 criticality statuses against official USGS/EU/BGS sources.
- Fill Supplementary Tables S2 and S7 manual literature-check columns.
- Confirm no API keys or private credentials are committed.
