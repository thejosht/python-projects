# Matching Strings by Similarity (Levenshtein Distance)

## Project goal

Given two independent lists of company names, I identified which records likely refer to the same real-world entity—even when the spelling, punctuation, or legal suffixes differ.  
This was achieve this by:

1. Loading the two raw CSV files (`companies_1.csv` and `companies_2.csv`).
2. Generating every possible pair of names between the lists (a cartesian join).
3. Scoring each pair with a Levenshtein-based _partial-ratio_ similarity metric (`thefuzz`).
4. Flagging pairs with high similarity (score ≥ 90) as potential matches.
5. Answering eight focused questions to validate the matching logic.

The result is a repeatable workflow that automates manual “is this the same company?” decisions—useful for vendor-master clean-ups, CRM deduplication, and any scenario where inconsistent naming blocks straightforward joins.

---

## Files

| File                       | Rows × Cols                                               | Description                                |
| -------------------------- | --------------------------------------------------------- | ------------------------------------------ |
| `companies_1.csv`          | 266 × 1                                                   | Master client list (column **CLIENT**)     |
| `companies_2.csv`          | 368 × 1                                                   | Candidate firm list (column **Firm Name**) |
| `levenshtein_8tasks.ipynb` | Notebook with the 8 numbered questions, ready for answers |

---

## Skills Demonstrated

| Pillar                    | Techniques                                    |
| ------------------------- | --------------------------------------------- |
| **String matching / NLP** | `thefuzz.partial_ratio`, Levenshtein distance |
| **Data wrangling**        | pandas cartesian product, boolean filtering   |
| **Custom functions**      | reusable `ratio_score` helper                 |
| **Exploratory analysis**  | counts, queries, spot-checking edge cases     |
| **Reproducible research** | clean Jupyter notebook, code+answers in-line  |
| **Performance awareness** | vectorised scoring rather than Python loops   |

---

## Answer Summary

| #   | Prompt (abridged)                                                   | Result from notebook                               |
| --- | ------------------------------------------------------------------- | -------------------------------------------------- |
| 1   | Create cartesian DataFrame (`CSV 1` × `CSV 2`)                      | ✅ `cartesian_df` built (97 888 rows)              |
| 2   | Add **Ratio Score** column (partial-ratio)                          | ✅ all rows scored 0-100                           |
| 3   | How many rows have **Ratio Score ≥ 90**?                            | **135** potential matches                          |
| 4   | Match for **AECOM**                                                 | _AECOM ↔ AECOM Technology Corporation_ (score 100) |
| 5   | Match for **Starbucks**                                             | _Starbucks ↔ Starbucks Corporation_ (score 100)    |
| 6   | Match for **Pinnacle West Capital Corp.**                           | Closest: _Ball Corporation_ (score 93)             |
| 7   | Matches for **County of Los Angeles Deferred Compensation Program** | 2 matches (score > 90)                             |
| 8   | Match status for **The Queens Health Systems**                      | Found → _The Queen’s Health Systems_ (score 96)    |

---

## How to Re-run

```bash
pip install "thefuzz[speedup]" pandas
jupyter notebook levenshtein_8Q.ipynb
```
