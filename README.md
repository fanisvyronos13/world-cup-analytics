# World Cup Analytics: What Actually Wins Tournaments?

A statistical analysis of 96 national teams across the 2014, 2018 and 2022 FIFA World Cups, extended with a Poisson regression model and Monte Carlo simulation to predict the 2026 tournament.

Built as a portfolio project by Fanis Vyronos, BSc Mathematics Statistics and Business, London School of Economics.

---

## Key Findings

- **Goal difference per game** is the strongest predictor of World Cup success (Spearman r = 0.718)
- **Possession % is not statistically significant** (r = 0.200, p = 0.051) — Germany 2018 had 73% possession and exited in the group stage
- **2022 was the most unpredictable tournament** in the dataset — all 5 biggest statistical underachievers came from the same year

---

## Poisson Model

Trained on 11,440 competitive international matches since 1990. Validated against 482 World Cup matches — correlation of 0.43 between predicted and actual goal difference, matching Goldman Sachs's reported benchmark exactly.

**2026 Win Probabilities:**

| Team | This Model | Goldman Sachs |
|---|---|---|
| Spain | 16.2% | 25.7% |
| Argentina | 10.0% | 14.3% |
| France | 7.6% | 18.9% |
| England | 5.7% | 5.0% |
| Brazil | 5.6% | 7.6% |

---

## Repository Contents

| File | Description |
|---|---|
| `worldcupanalysisfinalcode.html` | Full annotated notebook (36 cells) |
| `worldcup_master.csv` | Master dataset — 96 teams, 3 tournaments, 19 variables |
| `results.csv` | 49,450 international match results (Kaggle) |
| `WorldCup_Report_Final_Updated.pdf` | Full written report (~2,500 words) |

---

## Tools & Methods

Python · pandas · scipy · statsmodels · plotly · seaborn

Spearman correlation · Bonferroni correction · Poisson regression · Monte Carlo simulation · Elo ratings (eloratings.net)

---

## Data Sources

- Kaggle — international football results 1872–2026
- WhoScored — team statistics 2014 & 2018
- FIFA official records — 2022 tournament data
- eloratings.net — Elo ratings as of June 10, 2026


## Live Updates
Model re-runs after every gameweek → [View all updates](Updates)
