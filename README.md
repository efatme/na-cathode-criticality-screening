# Criticality-aware materials informatics of sodium-ion cathode candidate prioritization using computed electrode descriptors and text-mined literature evidence

This repository supports the submitted manuscript **NXSUST-D-26-01414** in *Next Sustainability*.

## Scope

This repository contains a reproducible, criticality-aware materials-informatics workflow for sodium-ion cathode candidate prioritization. The workflow combines Materials Project sodium-ion electrode records, conservative criticality-aware filtering, ChemDataExtractor-derived text-mined battery evidence, grouped cross-validation machine learning, feature-leakage auditing, and manuscript-ready figures/tables.

The study is a decision-support workflow. It does **not** experimentally validate cathodes and does **not** claim discovery of new cathode materials.

## Main counts

- Materials Project sodium-ion electrode records: 416
- Basic electrochemical screening pass: 164
- Hard-exclusion-free candidates: 112
- Conservative earth-abundant proxy candidates: 56
- Conservative candidates with exact CDE evidence: 18
- Deduplicated manuscript shortlist: 95

## Leakage-audited ML interpretation

Notebook 06 performs target-specific leakage auditing. Na-stoichiometry near-target features are removed for capacity and energy, and stability components are removed for the derived `stability_worst` target. The C-strict protocol is interpreted as a post-DFT decision-support protocol, not a pre-DFT discovery model.

## Repository structure

```text
01_mp_data_extraction.ipynb                    Materials Project extraction and initial processing
02_cde_evidence_matching.ipynb                 ChemDataExtractor-derived evidence matching
03_ml_protocols.ipynb                          Descriptor construction, screening, ML, and shortlist generation
04_figures_tables_manuscript_framing.ipynb     Manuscript tables and figure data
05_repository_submission_packaging.ipynb       Packaging utility notebook, not required for result reproduction
06_leakage_corrected_ml_and_submission_repair.ipynb  Leakage audit and corrected ML interpretation
data/processed/                                Main manuscript tables
data/figure_data/                              CSV files used to create figures
data/supplementary/                            Supplementary tables and leakage-audit files
figures/main_figures/                          Main figures as PNG and PDF
figures/supplementary_figures/                 Supplementary figures as PNG and PDF
manuscript_assets/                             Captions and claim-control text blocks
audit/                                         Output and repository audit files
```

## Run order

See [`RUN_ORDER.md`](RUN_ORDER.md). Notebook 05 is a packaging utility and is not required to reproduce the scientific results.

## Data availability

Processed datasets, figure-data files, and repository supporting files are available in this repository:

```text
https://github.com/efatme/na-cathode-criticality-screening
```

Materials Project source sodium-ion electrode records must be accessed through the Materials Project API subject to the Materials Project terms of use. ChemDataExtractor-derived source records should be obtained from the original cited battery text-mining resources.

## Code availability

Analysis notebooks and environment files are available in this public GitHub repository:

```text
https://github.com/efatme/na-cathode-criticality-screening
```

A DOI has not yet been minted for this initial public upload. If requested during review or revision, an archived release DOI can be added through Zenodo or an equivalent repository archive.

## License

- Code: MIT License, see [`LICENSE`](LICENSE).
- Processed data, figure data, and manuscript-derived tables: CC BY 4.0, see [`LICENSE_DATA.md`](LICENSE_DATA.md).

## Citation

Please cite the submitted manuscript and this repository. Citation metadata are provided in [`CITATION.cff`](CITATION.cff).

## Contact

Corresponding author: Md. Efatuzzaman Efat  
Email: efatuzzaman@gmail.com
