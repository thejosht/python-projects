# Google Play Store Data Wrangling & EDA

Welcome! This mini‑project takes the original **Google Play Store** dataset (10 k+ Android apps) from _messy_ → _tidy_ while answering a set of data‑wrangling questions. The companion [Jupyter notebook](playstore_cleaning.ipynb) shows every transformation step‑by‑step so you can follow along.

---

## 🔑 Skills Demonstrated (at a glance)

- **Data Inspection & Profiling** – quick `info()`, missing‑value heat‑maps, outlier scans.
- **Data Cleaning**
  - De‑duplicated app listings (kept highest‑review version)
  - Filtered impossible ratings (> 5) & cast to float
  - Parsed _Reviews_, _Size_, _Installs_, _Price_ → pure numerics (handled K / M suffixes, “+” signs, `$`)
  - Standardised category labels & trimmed stray whitespace
  - Imputed missing sizes with category medians
- **Data Analysis**
  - Top categories by counts & installs
  - Rating distribution, free vs paid comparisons
  - Leveraged vectorized pandas operations (arithmetic & unit conversion) to derive high-level business metrics from raw fields
  - Calculated total data transfer for the top Lifestyle app ≈ 490 TiB (APK size × installs), highlighting the scale of distribution.
- **Visual Storytelling** – concise matplotlib / seaborn charts embedded throughout
- **Reproducible Workflow** – clear, commented code in a single notebook

---

## 📊 Key Results

| Metric                 | Raw Data | After Cleaning |
| ---------------------- | -------- | -------------- |
| Row count              | 10 ,841  | 9 ,982         |
| Duplicate rows removed | —        | 483            |
| Ratings > 5            | 19       | 0              |
| Missing ratings        | 1 ,474   | 0              |
| Distinct categories    | 1 ,23    | 49             |

---

## 🚀 How to Reproduce

1. Clone / download this repo
2. `pip install -r requirements.txt` _(pandas, numpy, matplotlib, seaborn, jupyter)_
3. Launch JupyterLab and open **playstore_cleaning.ipynb**
4. Run all cells (takes < 30 s on a laptop)

---

## 🤝 Why It Matters

Cleaning real‑world data is 80 % of the job. This project **demonstrates** my ability to

- untangle messy, semi‑structured data,
- build repeatable, transparent pipelines, and
- surface actionable insights through clear visualisation & concise commentary.

Thanks for reading – feedback always welcome!
