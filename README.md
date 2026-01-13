# Avoidance-of-Rejuvenation-Supplementary-Materials

Packages:
python 3.12
numpy
matplotlib
seaborn
scikit-learn
pandas
scipy
SALib


Section 1: Setup & Data Generation
Cell 3: Monte_Carlo simulation dataframe. Creates df_results with 100,000 random parameter combinations. Computes derived quantities (X, p, λ, β, η, N, W, n0, nX, S) for the first model where lifespan X = (C·L)/(D-M). This is the foundational data cell for the first model analysis.

Section 2: First Model Analysis (depends on df_results)
Cell 4: Correlation heatmap
Cell 5: PCA analysis. Performs PCA on parameters to visualize clustering/relationships between model parameters in 2D space.
Cell 6: Age Distribution Histogram  from df_results 

Section 3: Global Sensitivity Analysis
Cell 8: Sobol Sensitivity Analysis. Shows main effects vs interaction effects for X = (C·L)/(D-M).

Section 4: Core Functions Definition
Cell 10: S0 Computation helper function. Defines compute_S0() function and computes optimal S0 ≈ 230.25.
Cell 11: All Core Functions used in next cells
Section 5: First Model Heatmaps
Cell 12: Survival Proportion Heatmap
Cell 13: X(μ, L) Heatmap

Section 6: Pathogen Model Analysis
Cell 16: Normalized Ns, Ni, W vs X (v=0.001)
Cell 17: Normalized Ns, Ni, W vs X (v=0.000149)
Cell 18: Ns, Ni vs X with X=18 Marker
Cell 19: Ns, Ni vs X for Different L Values
Cell 20: W vs X with X=18 Marker
Cell 21: W vs X for Different L Values

Section 7: Effect of Infection Rate β
Cell 22: W(X) for Different β
Cell 23: W(X) for Different β (n0 as parameter)
Cell 25: Ni, Ns at Specific β

Section 8: Optimal X Analysis 
Cell 28: X_max(W) vs β (Discontinuous)
Cell 29: X_max(W) vs β with n0 Sweep
Cell 30: Ns, Ni with Special Point
Cell 31: Defines solve_p_from_params_third_model() - alternative method to solve for p in the third model.

Section 9: Sensitivity Analysis for Pathogen Model
Cells 33-38: Sensitivity to μ, S0, M, F, m, C X_max(W) curves for 7 different μ values (±80% range).

Section 10: W Heatmaps (X vs n0) at Different β
Cells 39-47: Each generates a heatmap of W over (X, n0) space at a specific β value: β = 0.00001, 0.00006, 0.00013, 0.00029, 0.00062, 0.00134, 0.00289, 0.00622, 0.01340
Red dot marks the maximum W location.
