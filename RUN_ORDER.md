# Notebook run order

Run the notebooks in this order.

1. `01_mp_data_extraction.ipynb`  
   Materials Project sodium-ion electrode extraction, correction, filtering, and provenance logging.

2. `02_cde_evidence_matching.ipynb`  
   ChemDataExtractor battery database cleaning and exact formula-level literature-evidence matching.

3. `03_ml_protocols.ipynb`  
   Descriptor construction, Protocol A/B/C-strict ML, grouped cross-validation, candidate shortlist, and first-pass outputs.

4. `04_figures_tables_manuscript_framing.ipynb`  
   Manuscript tables, figure-data files, Plotly HTML figures, and initial manuscript framing.

5. `05_repository_submission_packaging.ipynb`  
   Repository package, submission statements, README, and manuscript-support files.

6. `06_leakage_corrected_ml_and_submission_repair.ipynb`  
   Feature-leakage audit, leakage-corrected ML metrics, stability permutation test, and reviewer-safe ML interpretation.

7. `07_repository_cleanup_figures_and_manuscript_assets.ipynb`  
   Final repository cleanup, journal-quality figures, supplementary tables, updated captions, and submission-ready package draft.

## Important notes

- Do not commit API keys, `.env` files, or private credentials.
- Full Materials Project raw data should be regenerated through the API according to the instructions in `data/raw/README_raw_data.md`.
- ChemDataExtractor evidence is text-mined literature evidence, not experimental validation.
- Protocol C-strict is a post-DFT decision-support protocol, not a pre-DFT discovery model.
