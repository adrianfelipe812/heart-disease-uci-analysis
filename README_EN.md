# Exploratory Analysis of Heart Disease | UCI Heart Disease

*Spanish version: [README.md](README.md)*

Statistical analysis in R of the **UCI Heart Disease** dataset (920 patients from Cleveland, Hungary, Switzerland and VA Long Beach). The project covers data quality assessment, missing-value treatment with Hot Deck imputation, descriptive statistics by disease severity (`num`, 0–4), exploratory associations and visualizations.

## Key points

- **Data quality first.** Missingness is not random: it depends on the clinical center. `ca` is missing in 66 % of records (≥ 96 % outside Cleveland), `thal` in 53 %, and every Swiss record reports cholesterol = 0, which is treated as missing before imputation.
- **Imputation.** Single Hot Deck imputation (`VIM`, fixed seed) after converting non-physiological zeros to `NA`.
- **Descriptive findings in this sample.** 63.22 % of men have `num ≥ 1`; among men with non-anginal chest pain the share is 44.37 %.
- **Visual analysis.** Histograms, boxplots by severity, scatter plots and a correlation heatmap.

## Limitations

These are sample descriptions, not clinical inferences. Single imputation does not propagate imputation uncertainty, and Pearson correlations with an ordinal outcome are exploratory only. Not a diagnostic tool.

## Reproduce

Requires R. Install the packages listed in the Spanish README and run `rmarkdown::render("informe_heart_disease.Rmd")`. The report reads `data/heart_disease_uci.csv` with a relative path.

**Data source:** Janosi, Steinbrunn, Pfisterer & Detrano. *Heart Disease*. UCI Machine Learning Repository. [DOI 10.24432/C52P4X](https://doi.org/10.24432/C52P4X) (CC BY 4.0).

**Tech:** R · dplyr · ggplot2 · VIM · naniar · R Markdown · **License:** CC BY 4.0
