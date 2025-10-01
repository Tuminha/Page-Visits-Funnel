<div align="center">

<h1>Page Visits Funnel</h1>

<p>Analyze the conversion funnel for Cool T-Shirts Inc. from visit → cart → checkout → purchase.</p>

<p>
  <a href="https://www.python.org/" target="_blank"><img alt="Python" src="https://img.shields.io/badge/Python-3.9%2B-3776AB?logo=python&logoColor=white"></a>
  <a href="https://jupyter.org/" target="_blank"><img alt="Jupyter" src="https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white"></a>
  <a href="https://pandas.pydata.org/" target="_blank"><img alt="pandas" src="https://img.shields.io/badge/pandas-Data%20Analysis-150458?logo=pandas&logoColor=white"></a>
</p>

<p>
  <a href="Page_Funnel_Visits.ipynb"><img alt="Open Analysis Notebook" src="https://img.shields.io/badge/Open-Analysis%20Notebook-4C9A2A?style=for-the-badge"></a>
  <a href="Page_Funnel_Visits_Solution.ipynb"><img alt="Open Solution Notebook" src="https://img.shields.io/badge/Open-Solution%20Notebook-8A2BE2?style=for-the-badge"></a>
  <a href="https://github.com/Tuminha/Page-Visits-Funnel/archive/refs/heads/main.zip" target="_blank"><img alt="Download ZIP" src="https://img.shields.io/badge/Download-ZIP-0A66C2?style=for-the-badge&logo=github"></a>
</p>

</div>

---

### Overview

This project builds a product funnel for Cool T-Shirts Inc. using real website event logs. We quantify how many users progress through each step and identify the weakest stage:

- Visit → Add to Cart → Checkout → Purchase

You will also compute the average time from first visit to purchase.

### Data

CSV files included in this repository:

- `visits.csv`: all users who visited the site
- `cart.csv`: users who added a t‑shirt to cart
- `checkout.csv`: users who initiated checkout
- `purchase.csv`: users who completed a purchase

Open `Page_Funnel_Visits.ipynb` to follow the analysis steps. A companion reference notebook is provided in `Page_Funnel_Visits_Solution.ipynb`.

### Tasks (Codecademy)

1. Inspect DataFrames (`print`, `.head()`)
2. Left-merge `visits` ↔ `cart`
3. Length of merged DataFrame
4. Count null `cart_time` and interpret
5. Percent of visitors who did not add to cart
6. Left-merge `cart` ↔ `checkout`; percent dropped before checkout
7. Merge all four steps (left merges) into `all_data`
8. Percent who reached checkout but did not purchase
9. Identify weakest funnel step and propose improvements
10. Add column: `purchase_time - visit_time`
11. View the new time delta column
12. Average time to purchase (`.mean()`)

### Quickstart

```bash
# 1) Create and activate a virtual environment (optional, recommended)
python3 -m venv .venv && source .venv/bin/activate

# 2) Install dependencies
python -m pip install --upgrade pip
pip install jupyter pandas numpy matplotlib seaborn

# 3) Launch Jupyter
jupyter notebook  # or: jupyter lab

# 4) Open the notebook
#    - Page_Funnel_Visits.ipynb
#    - Page_Funnel_Visits_Solution.ipynb (reference)
```

### What You'll Learn/Practice

- Left joins for stepwise funnels
- Null analysis to quantify drop-off
- Percentage conversion at each stage
- End-to-end time-to-purchase calculation
- Data quality issues: identifying when raw counts don't match funnel logic
- Using `.nunique()` vs `.sum()` for accurate user counts

### Key Insights

- **Data Quality Check**: Raw table counts can be misleading (e.g., 252 purchases > 226 checkouts)
- **Solution**: Use left merges and `.nunique()` on user_id for accurate funnel analysis
- **Learning**: Always validate data consistency before drawing conclusions

### Suggested Improvements (Next Steps)

- Parameterize the funnel steps and file names to re-use the notebook on other datasets
- Add visualizations: bar charts for stage conversion, Sankey diagram for flow, and distribution of time-to-purchase
- Export a concise summary report (Markdown/HTML) with key KPIs
- Add data validation checks to identify anomalies early

### Screenshots (Optional)

Add plots such as:

- Conversion by step
- Time to purchase distribution

### Acknowledgements

- Exercise inspired by Codecademy’s Page Visits Funnel project

### Contact

Created by Francisco Barbosa

- Email: <a href="mailto:cisco@periospot.com">cisco@periospot.com</a>
- X (Twitter): <a href="https://twitter.com/cisco_research" target="_blank">@cisco_research</a>

---

<div align="center">
  <sub>Made with ❤️ using Python, pandas, and Jupyter.</sub>
</div>


