# Notebook run order

Run the notebooks in this order to reproduce the submitted workflow.

1. `01_mp_data_extraction.ipynb`  
   Materials Project sodium-ion electrode extraction, correction, filtering, and provenance logging.

2. `02_cde_evidence_matching.ipynb`  
   ChemDataExtractor battery database cleaning and exact formula-level literature-evidence matching.

3. `03_ml_protocols.ipynb`  
   Descriptor construction, Protocol A/B/C-strict ML, grouped cross-validation, candidate shortlist, and first-pass outputs.

4. `04_figures_tables_manuscript_framing.ipynb`  
   Manuscript tables, figure-data files, figures, and initial manuscript framing.

5. `06_leakage_corrected_ml_and_submission_repair.ipynb`  
   Feature-leakage audit, leakage-corrected ML metrics, stability permutation test, and reviewer-safe ML interpretation.

## Important notes

- Do not commit API keys, `.env` files, or private credentials.
- Materials Project source data should be regenerated through the API according to `data/raw/README_raw_data.md`.
- ChemDataExtractor-derived evidence is text-mined literature evidence, not experimental validation.
- Protocol C-strict is a post-DFT decision-support protocol, not a pre-DFT discovery model.
