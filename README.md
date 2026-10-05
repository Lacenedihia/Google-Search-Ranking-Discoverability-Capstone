# Google Search Ranking & Discoverability: Capstone

> Does AI-optimized content rank better in search results? An analysis of ~105,000 content items across 38 clients.

Capstone project for the **FlyRank AI Machine Learning internship** (Jul–Sep 2026).

🔗 **Live report:** https://lacenedihia.github.io/Google-Search-Ranking-Discoverability-Capstone/

---

## Research question

Is **AI optimization** associated with better positions in Google search results, once we account for other factors such as **content length** and **keyword competitiveness**? And does that advantage hold up over time?

## Dataset

- **FlyRank ML Internship Warehouse** (Hugging Face)
- **105,810 content items** from **38 active clients** (out of 104 tracked)
- Queried with **DuckDB**

## Method

1. **Data exploration and cleaning** with DuckDB and Pandas
2. **Feature definition**: AI-optimization status, content length, keyword competitiveness, time since publication
3. **Baseline model** to set a reference error (MAE = **3.82** positions)
4. **Linear regression** estimating the effect of AI optimization while controlling for confounders
5. **5-fold grouped cross-validation**, grouped by client so that no client appears in both training and test folds (avoids leakage)
6. **Statistical testing** with SciPy
7. **Visualization** with Matplotlib and Plotly

## Key findings

- AI-optimized content ranks about **2.1 positions better** (coefficient **−2.07**, **p < 0.001**), even after controlling for content length and keyword competitiveness.
- This advantage **decays more slowly over time** than for non-optimized content.

## Limitations

- The analysis is **observational**: results show an **association**, not proof of causation.
- Results come from 38 clients and may not generalize to other sites or sectors.
- Search ranking is influenced by factors not captured in the dataset.

## Tech stack

`Python` · `DuckDB` · `Pandas` · `NumPy` · `Scikit-learn` · `SciPy` · `Matplotlib` · `Plotly` · `Jupyter` · `Git` · `GitHub Actions` (deployment)

## Repository structure

```
.
├── index.html            # Final capstone report (published with GitHub Pages)
├── README.md             # This file
└── .github/workflows/    # GitHub Actions: automatic static deployment
```

## Author

**Dihia Lacene**: Telecommunications engineer, Master's student in Signal and Image Processing (ULCO, France)

[GitHub](https://github.com/Lacenedihia) · [LinkedIn](https://www.linkedin.com/in/) · [Portfolio](https://lacenedihia.netlify.app/)
