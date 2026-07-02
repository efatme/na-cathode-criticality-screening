# Notebook run order

Run the notebooks in this order to reproduce the workflow.

1. `01_mp_data_extraction.ipynb`  
   Materials Project sodium-ion electrode extraction, correction, filtering, and provenance logging.

2. `02_cde_evidence_matching.ipynb`  
   ChemDataExtractor-derived battery literature-evidence cleaning and exact formula-level matching.

3. `03_ml_protocols.ipynb`  
   Descriptor construction, Protocol A/B/C-strict machine learning, grouped cross-validation, and candidate shortlist generation.

4. `04_figures_tables_manuscript_framing.ipynb`  
   Manuscript tables, figure-data files, and initial manuscript-support outputs.

5. `05_repository_submission_packaging.ipynb`  
   Repository packaging utility. This notebook creates repository support files and submission assets.

6. `06_leakage_corrected_ml_and_submission_repair.ipynb`  
   Feature-leakage audit, leakage-corrected ML metrics, stability permutation test, and reviewer-safe ML interpretation.

## Notes

- Do not commit API keys, `.env` files, or private credentials.
- Materials Project source data should be regenerated through the Materials Project API according to the instructions in `data/raw/README_raw_data.md`.
- ChemDataExtractor-derived evidence is treated as text-mined literature signal only, not experimental validation.
- Protocol C-strict is a post-DFT decision-support protocol, not a pre-DFT discovery model.
