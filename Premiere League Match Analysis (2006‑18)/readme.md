# Premier League Data Cleaning & Exploratory Analysis

> One notebook, one raw CSV, a lot of wrangling.

---

## 📑 Project Brief

I started with a **15‑year dump of Premier League match results** that was riddled with typos, stray quotes, unknown seasons ("?"), and invalid result codes.\
The goal was to **clean the dataset, validate every row, and surface quick insights**—entirely in Python.

## 🗃️ Data Sources

| File                           | Description                                    |
| ------------------------------ | ---------------------------------------------- |
| `premier‑league‑data.csv`      | Raw match data (2006‑07 → 2017‑18)             |
| `premier‑league-project.ipynb` | Jupyter notebook with all cleaning + EDA steps |

## 🛠️ Key Steps & Fixes

1. **Column tidy‑up** — stripped stray quote marks from the header row.
2. **Season sanity check** — converted unknown seasons (`?`) to a sentinel value ("Unknown season").
3. **Result repair** — auto‑recalculated any missing / wrong _H / A / D_ flags using scorelines.
4. **Feature engineering** — added `goal_diff`, match outcome booleans, and rolling win % by club.
5. **Exploratory visuals** — quick plots of biggest goal swings, top‑scoring teams per season, etc.

## 🚀 Skills Demonstrated

- **Python 3, pandas 2** → chaining, vectorised ops, `loc` updates, boolean masks.
- **Data cleaning & validation** → missing‑value imputation, categorical re‑mapping.
- **Feature engineering** → new columns on the fly without for‑loops.
- **Jupyter storytelling** → clear Markdown narrative + commented code cells.
- **Working with a sports data set** → effectivivly apply industry data science practices in a sport related context.

```

## 📂 Repo Layout

```

.
├── premier‑league‑data.csv
├── premier‑league-project.ipynb
├── README.md

```

---
```
