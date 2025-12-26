# The Collapse of the American Dream: From "Rags to Riches" to the "Ragged and the Rich"

**Capston Project — Wharton Global Youth Data Science Academy**  
**Authors:** John Wu, Connie Lu, Smriti Vijay, Gwen Gao, Alvin Li  

---

## Project Overview
This project investigates how the promise of the American Dream has evolved over time and explores factors that influence social mobility. Using datasets from the US and international sources, we modeled the relationships between economic inequality, corruption perception, healthcare, education, and social mobility outcomes.

**Key Research Questions:**
- How accurately does the current American Dream provide upward mobility?  
- How do economic and social policies affect social mobility across countries?  
- What lessons can the U.S. learn from other nations to improve social mobility?

---

## Repository Structure
```
data/
  WDS Project.xlsx      # Raw dataset used for analysis
  Clean_Data.csv        # Cleaned dataset

output/
  analysis.html         # Compiled HTML of analysis.Rmd
  report.html           # Compiled HTML of report.Rmd
  presentation.pptx     # Presentation slides

analysis.Rmd            # Full R Markdown with code, cleaning, and modeling
report.Rmd              # Clean narrative version for presentation
final.Rproj             # RStudio project file

README.md               # Project overview and instructions
REFERENCES.md           # List of all data sources and references
```

---

## Methodology

1. **Data Collection**  
   - Datasets from FRED, OECD, World Bank, Numbeo, Transparency International, Our World in Data, and more.

2. **Data Cleaning & Preprocessing**  
   - Performed entirely in `analysis.Rmd` — no external “cleaned” CSV required.  
   - Steps include subsetting, log-transformations, and variable selection.

3. **Modeling**  
   - Techniques: Linear Models (LM), LASSO, Relaxed LASSO, Decision Trees, Random Forest, XGBoost  
   - Predicting **Social Mobility Index**, **Poverty Rate**, and **GDP per Capita**

4. **Model Selection**  
   - Selected based on testing error, interpretability, and statistical significance.

---

## Key Findings

- **Social Mobility Index:** Influenced by corruption perception, wealth share of top 1%, and GINI coefficient.  
- **Poverty Rate:** Affected by healthcare index, wealth distribution, and welfare spending.  
- **GDP per Capita:** Strongly predicted by corruption perception.

> See `output/report.html` for visualizations and detailed results.

---

## Limitations

- Small sample size (24 countries) limits predictive power.  
- Focused mainly on high-income countries; non-OECD countries are underrepresented.  
- Some data points may be outdated.

---

## Future Work

- Expand analysis to more countries and time periods.  
- Examine real socio-economic effects of policy changes.  
- Evaluate longitudinal trends in social mobility.

---

## How to Run

1. Open `final.Rproj` in RStudio.  
2. Open `analysis.Rmd` and knit to generate results.  
3. Keep the raw dataset `data/WDS Project.xlsx` in the `data/` folder.

---

## References

- FRED, OECD, Our World in Data, Numbeo, Transparency International, World Bank, N26, World Population Review  
- See [References](REFERENCES.md) for more detailed sources.
---

**Note:** Rendered outputs in `output/report.html` may not knit perfectly on different machines due to package version differences. All code and preprocessing steps are reproducible via `analysis.Rmd`.
