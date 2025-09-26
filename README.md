Two short workflows demonstrating a clean ingest → process → analyze pipeline.

**Question 1 (Frailty):** small clinical-style dataset (hand-grip strength) — standardize units, engineer BMI & age groups, encode frailty, run EDA, compute correlation, and save a short report.

**Question 2 (Student performance):** Preprocess the students' dataset, handle missing values, produce 5 publication-ready figures (V1–V5), and short interpretations for each.

Both parts produce well-organized outputs (CSV, PNGs, and a findings report), allowing graders to inspect the code, results, and explanations easily.
> Note: Make sure folder names used by the notebooks (`result_dir`, `output`, `reports`, etc.) are real folders you upload.
----

## Key files & outputs

**Question 1**

- `question1.ipynb` — ingestion, unit standardization, feature engineering, encoding, and EDA.
- `output/clean_data.csv` — cleaned dataset with `Height_m`, `Weight_kg`, `BMI`, `AgeGroup`, `Frailty_binary`, and one-hot AgeGroup columns.
- `reports/findings.md` — summary table (mean/median/std) and the calculated correlation between `Grip_kg` and `Frailty_binary`.
- 
**Question 2**

- `question2.ipynb` — preprocessing, imputation, plotting code.
- `result_dir/` — PNG plots:
  - `V1_gender_boxplots.png`
  - `V2_test_prep_math.png`
  - `V3_lunch_avg.png`
  - `V4_subject_correlation.png`
  - `V5_math_reading_trend.png`
- `reports/visualizations.md` — five brief (5–8 sentence) descriptions for each figure.
**Run in Colab**

Upload the repo or open the notebook from GitHub in Colab.

Run the notebook top-to-bottom.

Refresh the Colab Files pane to view created folders and saved images.

**Run locally**
git clone the repo.

Start Jupyter: jupyter notebook and open each notebook.

Run all cells; outputs will be saved in output/, result_dir/, and reports/.

**Notes for graders**

All figures were saved as 800×600 px and 300 DPI for print/readability.

Notebooks were designed to be standalone: they take raw CSVs from the working directory and output results to plain-named directories.

Adjust top-of-notebook path variables prior to running if you find a path mismatch (OS or varying folder name).

If you'd like, I can:
generate the reports/findings.md and reports/visualizations.md content from your results, or
Generate a ready-to-upload zip for final submission.

**Requirements**

Python 3.8+

pandas, numpy, matplotlib, seaborn
