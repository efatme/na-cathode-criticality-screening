# Figure captions

## Figure 1. Reproducible criticality-aware sodium-ion cathode prioritization workflow.
Schematic of the integrated decision-support workflow. Materials Project sodium-ion electrode records are combined with ChemDataExtractor text-mined battery evidence and a criticality-aware filtering layer. Three descriptor protocols are evaluated under grouped cross-validation, and Notebook 06 adds feature-leakage auditing and leakage-corrected ML metrics. The output is a deduplicated 95-entry shortlist intended for follow-up prioritization, not experimental validation.

## Figure 2. Candidate screening funnel.
Stage-by-stage reduction from the initial Materials Project sodium-ion electrode records to the sustainability-aware candidate subsets and the final manuscript shortlist. The funnel should be interpreted as a transparent prioritization workflow. Candidate loss at each stage reflects applied screening criteria, hard-exclusion rules, conservative earth-abundance proxy filtering, and exact text-mined evidence availability.

## Figure 3. Family-level screening and text-mined evidence summary.
Family-level comparison of total records, basic electrochemical screening passes, hard-exclusion-free candidates, conservative candidates, and exact ChemDataExtractor evidence matches. Phosphate/NASICON-like entries dominate the conservative candidate pool, whereas transition-metal-oxide-like entries show the strongest exact text-mined literature-evidence coverage. Zero exact matches for sulfate-like and silicate-like families should be interpreted cautiously because exact formula matching can undercount literature variants.

## Figure 4. Leakage-corrected C-strict grouped-CV performance.
Grouped cross-validation performance for the C-strict post-DFT decision-support protocol after target-specific leakage treatment. Na-stoichiometry near-target features were removed for gravimetric capacity and energy analyses, and charged/discharged stability components were removed for the derived stability_worst target. Voltage and capacity remain useful after leakage audit; energy is moderate; stability is weak and retained only as an auxiliary cautionary result.

## Figure 5. Candidate voltage-capacity-energy landscape.
Voltage-capacity scatter map for the 95-entry deduplicated manuscript shortlist. Point size scales with gravimetric energy, and point grouping indicates preliminary chemistry family. The landscape is intended to support candidate prioritization by showing trade-offs between voltage, capacity, energy, chemistry family, and literature-evidence status. It does not represent experimental validation.

## Figure 6. C-strict feature importance after leakage audit.
Top feature importances from C-strict models after Notebook 06 leakage auditing. Feature importance is used for diagnostic interpretation only, not causal inference. Capacity and energy feature rankings should be interpreted together with Supplementary Tables S3 and S4, which identify Na-content near-target descriptors and report leakage-corrected metrics.
