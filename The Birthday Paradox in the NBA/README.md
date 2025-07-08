# NBA Birthday Paradox — 2024-25 Season 🎂🏀

This project estimates how likely it is that a **12-player NBA roster** contains at least two players who share a birthday, then compares the classic Birthday-Paradox curve with the _actual_ 2024-25 rosters.

| File                                   | Purpose                                      |
| -------------------------------------- | -------------------------------------------- |
| **nba_players_2024-25.csv**            | Clean roster data (name · team · birthdate). |
| **nba_birthday_paradox_2024-25.ipynb** | End-to-end analysis notebook.                |
| **README.md**                          | Project overview (you’re reading it).        |

---

## Key Skills Demonstrated 🛠️

1. **Data engineering** — robust CSV ingestion, datetime parsing, feature engineering
2. **Exploratory analysis** — league-wide & per-team duplicate-birthday counts
3. **Probability & simulation** — vectorised NumPy Monte-Carlo (10 000 ×)
4. **Visual storytelling** — Matplotlib curve + real-NBA datapoint annotation
5. **Performance** — zero Python loops inside core simulation (pure NumPy)
6. **Software craftsmanship** — clean notebook narrative, PEP-style code, Git-tracked assets

---

## Analysis Workflow

| Step                         | Description                                             |
| ---------------------------- | ------------------------------------------------------- |
| **1 Load data**              | Read the CSV, cast `birthdate` → `datetime`.            |
| **2 Engineer feature**       | Create `Birthday` (`MM-DD`) for collision checks.       |
| **3 League scan**            | Count duplicate birthdays among all active players.     |
| **4 Monte-Carlo simulation** | Compute P(shared birthday) for roster sizes 5-30.       |
| **5 Empirical check**        | Evaluate each team’s first-12 players; flag duplicates. |
| **6 Visualise & compare**    | Plot theoretical curve and overlay real NBA datapoint.  |

---

## League-Wide Summary — 2024-25 Roster Data

| #     | Question                                                           | Answer                                                   |
| ----- | ------------------------------------------------------------------ | -------------------------------------------------------- |
| **1** | How many players were analysed?                                    | **575** active players (rosters + free agents)           |
| **2** | How many unique birthdays are represented?                         | **290** distinct **MM-DD** combinations                  |
| **3** | How many players share a birthday with someone else?               | **285** players (575 − 290) have at least one duplicate  |
| **4** | Most common birthday & count?                                      | **June 19 / June 29 / Aug 26** — each occurs **6** times |
| **5** | Simulated P(shared birthday) for a 12-player group (10 000 trials) | **0.16** ≈ **16 %**                                      |
| **6** | Teams with duplicate birthdays in their first-12 players           | **4 / 30** teams                                         |
| **7** | Empirical probability (real NBA rosters, n = 12)                   | **4 ÷ 30 ≈ 0.13 → 13 %**                                 |

Real-world probability (13 %) sits a bit below the theoretical 16 % curve, hinting that player birthdays aren’t perfectly uniform.

---

## Answer Table — Notebook Prompts (2024-25)

| #       | Prompt (abridged)                                       | Answer                                                                                                 |
| ------- | ------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| **Q 1** | Birthday-paradox probability for **n = 10**             | **≈ 11 %** (0.114 from 20 000 Monte-Carlo trials)                                                      |
| **Q 2** | Birthday-paradox probability for **n = 15**             | **≈ 25 %** (0.249 from 20 000 trials)                                                                  |
| **Q 3** | Define `birthday_probability(n)`                        | Function returns Monte-Carlo P(shared birthday) for roster size `n` (see notebook).                    |
| **Q 4** | Display the new `Birthday` column                       | Added `Birthday = Birth Date.dt.strftime('%m-%d')`; first rows show e.g. Precious Achiuwa → **09-19**. |
| **Q 5** | Duplicate birthdays on **Boston Celtics**               | **03-03** – _Jayson Tatum_, _Jordan Walsh_.                                                            |
| **Q 6** | Duplicate birthdays on **Cleveland Cavaliers**          | **01-26** – _Darius Garland_, _Isaac Okoro_<br>**12-02** – _De’Andre Hunter_, _Jaylon Tyson_.          |
| **Q 7** | Players sharing a birthday with **Ivica Zubac** (03-18) | _Devin Carter_ (SAC), _Kris Dunn_ (LAC), _Jesse Edwards_ (MIN), _Skal Labissière_ (FA)                 |

---

## Quick Start

```bash
pip install pandas numpy matplotlib        # 1  install deps
jupyter notebook nba_birthday_paradox_2024-25.ipynb   # 2  run notebook
```
