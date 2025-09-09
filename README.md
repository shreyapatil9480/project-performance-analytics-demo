# Project Performance Analytics

This repository contains a **synthetic project management dataset** and an accompanying analysis notebook designed to showcase skills relevant to business analysis, program management and data analysis roles.  The goal of this project is to demonstrate how to turn raw data into insights using Python, exploratory data analysis and machine learning.

## Overview

Modern program and portfolio managers rely on data to track key metrics such as budgets, timelines, risk scores and team sizes.  To simulate this environment we generated a fictional dataset that captures 1,000 projects across several domains (Marketing, Operations, IT, HR and Finance).  Each record includes:

| Column | Description |
|---|---|
| `project_id` | Unique identifier for the project |
| `project_type` | Type of project (Marketing, Operations, IT, HR, Finance) |
| `start_date` | Planned project start date |
| `planned_duration_days` | Planned duration in days |
| `actual_duration_days` | Actual duration in days |
| `end_date` | Actual end date (computed from `start_date` + `actual_duration_days`) |
| `budget_usd` | Project budget in US dollars |
| `team_size` | Number of people assigned to the project |
| `complexity_level` | A categorical measure (1–10) of overall complexity |
| `risk_score` | Risk score between 0 and 1 (higher values indicate greater risk) |
| `status` | Whether the project finished on time (`OnTime`) or behind schedule (`Delayed`) |
| `satisfaction_score` | Stakeholder satisfaction on a 1–5 scale (simulated based on timeliness and noise) |

The dataset is saved as `project_data.csv` in the root of this repository.

## What’s in the notebook?

The Jupyter notebook `analysis.ipynb` walks through a typical analytical workflow:

1. **Loading the data** – using pandas to inspect the structure of the dataset.
2. **Exploratory data analysis (EDA)** – summary statistics and visualizations to understand distributions and relationships (e.g., project type counts, budget distribution and correlation matrix).
3. **Data preprocessing** – encoding categorical variables and preparing a modelling dataset.
4. **Predictive modelling** – training a random forest classifier to predict whether a project will be delayed based on the planned vs. actual durations, budget, team size, complexity, risk score and project type.  Model performance metrics (accuracy, classification report and confusion matrix) are provided along with a feature importance plot.
5. **Insights** – commentary on which factors most strongly correlate with project delays and high-level conclusions.

This end‑to‑end example highlights proficiency with:

- Data wrangling in pandas
- Visualization with seaborn/matplotlib
- Supervised learning using scikit‑learn
- Communicating results in a reproducible notebook

## Getting started

To run the analysis yourself, clone this repository and install the required dependencies:

```bash
# clone the repository (replace with your preferred directory)
git clone https://github.com/shreyapatil9480/project-performance-analytics-demo.git
cd project-performance-analytics-demo

# create a virtual environment (optional but recommended)
python -m venv .venv
source .venv/bin/activate  # On Windows use `.venv\Scripts\activate`

# install dependencies
pip install -r requirements.txt

# start Jupyter to explore the notebook
jupyter notebook analysis.ipynb
```

You can also open the notebook in JupyterLab or VS Code.  All of the required libraries are specified in `requirements.txt`.

## Repository structure

```
├── project_data.csv     # synthetic dataset
├── analysis.ipynb       # Jupyter notebook with EDA and modelling
├── requirements.txt     # list of Python dependencies
└── README.md            # this documentation
```

## Why this project?

Recruiters and hiring managers look for evidence that candidates can translate business questions into analytical tasks.  By working through this project you will demonstrate:

- An understanding of key program management metrics (budgets, schedules, risk and complexity).
- The ability to tell a story with data through charts and narratives.
- Experience building a machine learning model to predict real business outcomes.

Feel free to extend the dataset, try alternative models, or incorporate other variables (e.g., resource allocation or cost variance).  Contributions via pull requests are welcome!

---

© 2025 shreyapatil9480.  This project is provided for educational purposes.
