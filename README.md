# IPL Data Analysis

## Project Overview

This repository performs exploratory and analytical work on Indian Premier League (IPL) match and delivery data using Python. The project ingests raw IPL datasets, cleans and transforms the data, derives batting and bowling insights, and exports summary tables to CSV and Excel files.

## Repository Structure

- `deliveries.csv` — ball-by-ball IPL delivery data.
- `matches.csv` — match-level IPL metadata.
- `numpytask.ipynb` — NumPy-based analysis notebook with core calculations such as total runs per match, top batters, strike rate, economy, boundary stats, and death-over insights.
- `pandastask.ipynb` — Pandas-based end-to-end analysis pipeline with ingestion, cleaning, transformation, deeper analysis, insights, and export to CSV/Excel.
- `ipl_analysis.xlsx` — consolidated Excel workbook generated from the notebook exports.
- `output/` — folder containing exported CSV summaries:
  - `death_overs.csv`
  - `economy.csv`
  - `runs_per_match.csv`
  - `strike_rate.csv`
  - `team_scores.csv`
  - `top_batters.csv`

## Key Analyses

The project covers the following analytical themes:

1. Data ingestion and validation of IPL deliveries and matches.
2. Match-level scoring analysis, including total runs per match and highest-scoring games.
3. Batter performance summaries: top run-scorers, strike rates, boundary counts, and consistency.
4. Bowler performance summaries: economy rate and dot-ball influence.
5. Over-level scoring trends, including powerplay (overs 1–6) and death overs (overs 16–20).
6. Boundary analysis, team performance in death overs, and toss impact on match outcomes.
7. Export of cleaned results to CSV and an Excel workbook for easy reporting.

## How to Run

1. Install dependencies:
   - `pandas`
   - `numpy`
   - `openpyxl`

   Example:
   ```bash
   pip install pandas numpy openpyxl
   ```

2. Open `pandastask.ipynb` in Jupyter Notebook / JupyterLab.
3. Run the notebook cells from top to bottom.
4. The notebook creates exported files in the `output/` folder and writes a consolidated Excel workbook at `ipl_analysis.xlsx`.

## Notes on Analysis

- `numpytask.ipynb` is focused on raw NumPy operations and quick summary statistics for early-stage analysis.
- `pandastask.ipynb` contains a more robust Pandas workflow with cleaning, transformation, merged dataset construction, and richer exploratory outputs.
- The export stage writes multiple summary tables to both CSV and Excel for downstream sharing or visualization.

## Output Files

The project generates these deliverables:

- `output/runs_per_match.csv` — total runs in each match.
- `output/top_batters.csv` — top run-scorers.
- `output/strike_rate.csv` — batter strike rates with minimum balls faced.
- `output/economy.csv` — bowler economy rates.
- `output/team_scores.csv` — team scores by match.
- `output/death_overs.csv` — death-over scoring leaders.
- `ipl_analysis.xlsx` — consolidated workbook containing the above summaries and additional sheets like consistent batters, boundary leaders, dot ball leaders, runs per over, and season trends.

## Recommended Next Steps

- Add visualizations for run distributions, team comparisons, and over-by-over scoring.
- Expand the analysis to include player strike rates by season and venue-level batting conditions.
- Build an interactive dashboard using Plotly Dash, Streamlit, or Power BI.
