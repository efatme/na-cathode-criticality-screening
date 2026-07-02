# Updated leakage-aware ML interpretation for manuscript

The original C-strict model should not be presented as a clean pre-DFT predictor for capacity or energy. 
The feature-leakage audit identifies `comp__frac_Na`, `fracA_charge`, and `fracA_discharge` as near-target Na-stoichiometry descriptors for `capacity_grav`; because `energy_grav` is derived from capacity and voltage, the same features are also target-adjacent for energy.

In the full-feature C-strict setting, the capacity model gave R2 = 0.884 and Spearman = 0.954. 
After removing Na-stoichiometry near-target features, the leakage-corrected C-strict capacity result was R2 = 0.844 and Spearman = 0.885. 
The full-feature C-strict energy model gave R2 = 0.610 and Spearman = 0.865; after the same leakage correction, energy gave R2 = 0.571 and Spearman = 0.837.

Therefore, the manuscript should frame the full C-strict capacity/energy models as post-DFT reconstruction or decision-support models, not as fair pre-DFT discovery predictors. The leakage-corrected metrics should be reported as the reviewer-safe estimate of predictive performance after removing Na-stoichiometry near-target variables.

For `average_voltage`, the target-specific clean C-strict model gave R2 = 0.768. For `stability_worst`, the target-specific clean C-strict model gave R2 = 0.180. The stability model should remain an auxiliary cautionary result. The permutation test for `stability_worst` returned empirical p-value = 0.0010; this should be interpreted as evidence that the signal is above shuffled-label null only if p < 0.05, but not as evidence that stability prediction is strong enough for candidate ranking.

Recommended wording:

“Because gravimetric capacity is directly related to Na stoichiometry, we report C-strict capacity and energy performance both with and without Na-content near-target features. The full-feature C-strict models are interpreted as post-DFT decision-support reconstruction models, whereas the leakage-corrected results provide a stricter estimate of predictive performance. Stability prediction remains substantially weaker than voltage, capacity, and energy prediction and is therefore used only as an auxiliary cautionary indicator.”
