# Week 7 Codex CLI Assignment: Ames Housing Analysis

**Codex session date:** October 18, 2026

## Analytical question

How does above-ground living area affect home sale prices in Ames, Iowa, and does the relationship differ by neighborhood?

## Project overview

This project uses the AmesHousing dataset to examine the relationship between above-ground living area (`Gr Liv Area`) and sale price (`SalePrice`), including how that relationship varies by neighborhood. The provided CSV contains 2,930 home sales and 82 columns. The analysis is documented in a Jupyter Notebook and uses Python with pandas, NumPy, matplotlib, and seaborn.

## Verified findings

Across all 2,930 homes, living area has a positive linear association with sale price (Pearson *r* = **0.707**). The association is positive in each of the five largest neighborhoods, but varies in strength: CollgCr has the strongest correlation (*r* = **0.800**), followed by Somerst (**0.683**), OldTown (**0.677**), NAmes (**0.659**), and Edwards (**0.528**). In the neighborhood summary, NoRidge has the highest average sale price (**$330,319.13**; 71 homes) and MeadowV the lowest (**$95,756.49**; 37 homes). These results describe associations in the dataset; they do not establish that larger living area causes higher prices.

## Methods

The notebook loads the CSV, selects living area, sale price, and neighborhood, validates numeric fields, and checks missing, duplicate, and nonpositive values. All 2,930 observations were retained; no outliers were removed. It calculates house counts, mean and median sale prices, and mean living area by neighborhood. Scatterplots with linear trend lines show all homes and separate panels for the five largest neighborhoods. Pearson correlations quantify the overall linear association and the association within each of those five neighborhoods.

## Repository contents

- `AmesHousing-1.csv` — original dataset.
- `analysis/ames_housing_analysis.ipynb` — data loading, cleaning, neighborhood summary, visualizations, correlations, and findings.
- `analysis/neighborhood_summary.csv` — neighborhood-level summary statistics.
- `analysis/living_area_sale_price_all_homes.png` — scatterplot and overall trend line.
- `analysis/living_area_sale_price_top_neighborhoods.png` — neighborhood comparison panels.
- `prompts/codex-transcript.md` — assignment prompt history.
- `log/ai-workflow-log.md` — AI workflow log.
- `reflection.md` — assignment reflection.

## Limitations

Pearson correlation measures linear association and does not account for other factors such as home quality, age, or lot size. Extreme observations may influence the fitted trend lines; they were retained, and their influence was not separately quantified. Neighborhood sample sizes differ, so estimates for smaller groups may be less stable. Neighborhood-specific correlations are reported for the five largest neighborhoods only.
