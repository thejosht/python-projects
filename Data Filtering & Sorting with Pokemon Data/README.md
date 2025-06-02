# Pokémon Filtering & Sorting – Answers

This repository records my solutions to the **Practising Filtering & Sorting with Pokémon** project.  
It uses the canonical 721‑row Pokémon stat dataset (pokemon.csv).  
Run `pokemon_filtering_sorting.ipynb` to se my work.

---

Key Skills Demonstrated 🔍:

<<<<<<< HEAD
  1. Data wrangling: load CSV, inspect dtypes, tidy columns

  2. Filtering & Boolean logic: build masks with &, |, isin

  3. Sorting & ranking: sort_values, nlargest, percentile cuts

  4. Aggregation: quick counts with groupby, value_counts

  5. Reusable subsets: save filtered frames (slow_pokemons_df, legendary_df, …)

  6. EDA & outlier spotting: basic stats to flag extremes

  7. Jupyter Notebook craftsmanship: clear cell titles, Markdown narration

  8. Git + GitHub: commit data, code, README, Issue form
=======
1. Data wrangling: load CSV, inspect dtypes, tidy columns

2. Filtering & Boolean logic: build masks with &, |, isin

3. Sorting & ranking: sort_values, nlargest, percentile cuts

4. Aggregation: quick counts with groupby, value_counts and etc

5. EDA & outlier spotting: basic stats to flag extremes

6. Jupyter Notebook craftsmanship: clear cells and efficient use of the Jupyter note books environment

7. Git + GitHub: commit data, code, README, Issue form
>>>>>>> 1ccc32c (Update README and notebook with Final answers)

---

Answers:

| #   | Prompt (abridged)                    | My Answer                   |
| --- | ------------------------------------ | --------------------------- |
| 1   | Attack > 150                         | A1: 18                      |
| 2   | Speed ≤ 10 DataFrame                 | A2: 5                       |
| 3   | Sp. Def ≤ 25                         | A3: 18                      |
| 4   | All Legendary Pokémon                | A4: df.loc[df['Legendary']] |
| 5   | High Def / Low Atk outlier           | A5: Shuckle                 |
| 6   | Fire & Flying count                  | A6: 6                       |
| 7   | All Poison types count               | A7: 62                      |
| 8   | Strongest Def. among Ice (Type 1)    | A8: Avalugg                 |
| 9   | Most common Type 1 among Legendaries | A9: Psychic                 |
| 10  | Strongest Water (Gen 1‑3)            | A10: KyogrePrimal Kyogre    |
| 11  | Strongest Dragon (Gen 5‑6)           | A11: KyuremBlack Kyurem     |
| 12  | Powerful Fire (>100 Atk) DataFrame   | A12: Table for A12 in ipynb |
| 13  | Water **and** Flying DataFrame       | A13: Table for A13 in ipynb |
| 14  | Legendary Fire selected cols         | A14: Table for A14 in ipynb |
| 15  | Slowest 5 % & Fastest 5 %            | A15: Table for A15 in ipynb |
| 16  | Ultra‑Powerful Legendary             | A16: MewtwoMega Mewtwo X    |
