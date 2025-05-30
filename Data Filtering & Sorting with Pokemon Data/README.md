# Pokémon Filtering & Sorting – Answers

This repository records my solutions to the **Practising Filtering & Sorting with Pokémon** project.  
It uses the canonical 721‑row Pokémon stat dataset (pokemon.csv).  
Run `pokemon_filtering_sorting.ipynb` to se my work.

---

Key Skills Demonstrated 🔍:

Data wrangling: load CSV, inspect dtypes, tidy columns
Filtering & Boolean logic: build masks with &, |, isin
Sorting & ranking: sort_values, nlargest, percentile cuts
Aggregation: quick counts with groupby, value_counts
Reusable subsets: save filtered frames (slow_pokemons_df, legendary_df, …)
EDA & outlier spotting: basic stats to flag extremes
Jupyter Notebook craftsmanship: clear cell titles, Markdown narration
Git + GitHub: commit data, code, README, Issue form

---

| #   | Prompt (abridged)                    | My Answer |
| --- | ------------------------------------ | --------- |
| 1   | Attack > 150                         | A1:       |
| 2   | Speed ≤ 10 DataFrame                 | A2:       |
| 3   | Sp. Def ≤ 25                         | A3:       |
| 4   | All Legendary Pokémon                | A4:       |
| 5   | High Def / Low Atk outlier           | A5:       |
| 6   | Fire & Flying count                  | A6:       |
| 7   | All Poison types count               | A7:       |
| 8   | Strongest Def. among Ice (Type 1)    | A8:       |
| 9   | Most common Type 1 among Legendaries | A9:       |
| 10  | Strongest Water (Gen 1‑3)            | A10:      |
| 11  | Strongest Dragon (Gen 5‑6)           | A11:      |
| 12  | Powerful Fire (>100 Atk) DataFrame   | A12:      |
| 13  | Water **and** Flying DataFrame       | A13:      |
| 14  | Legendary Fire selected cols         | A14:      |
| 15  | Slowest 5 % & Fastest 5 %            | A15:      |
| 16  | Ultra‑Powerful Legendary             | A16:      |
