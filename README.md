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

**Latest Win Probabilities — After Gameweek 2:**

| Team | Pre-tournament | After GW1 | After GW2 |
|---|---|---|---|
| Spain | 16.2% | 13.9% | 13.5% |
| Argentina | 10.0% | 11.3% | 11.6% |
| France | 7.6% | 8.2% | 9.2% |
| England | 5.7% | 7.5% | 6.2% |
| Brazil | 5.6% | 5.3% | 4.9% |

Model re-runs after every gameweek → [View all updates](Updates)

---

## New: Qualification Model

Built for the 2026 group stage — simulates Gameweek 3 10,000 times using real GW2 standings and Elo ratings. Outputs qualification probability for all 48 teams via two routes: finishing top 2, or sneaking through as one of the best 8 third-place teams.

**Key finding:** Senegal sit on 0 points after 2 games but still have a 44% chance of qualifying — because finishing 3rd in a group with France and Norway is worth more than finishing 3rd in a weaker group.

---

## Live Updates

Model re-runs after every gameweek using updated Elo ratings from eloratings.net → [View all updates](Updates)

---

## Repository Contents

| File | Description |
|---|---|
| `worldcupanalysisfinalcode.html` | Full annotated notebook (36+ cells) |
| `worldcup_master.csv` | Master dataset — 96 teams, 3 tournaments, 19 variables |
| `results.csv` | 49,450 international match results (Kaggle) |
| `WorldCup_Report_Final_Updated.pdf` | Full written report (~2,500 words) |
| `gameweek2_probabilities.html` | Win probability chart after GW2 |
| `qualification_probabilities.html` | Round of 32 qualification — all 48 teams |
| `third_place_battle.html` | Third place battle — 12 groups, 8 spots |
| `group_standings_projected.html` | Projected final group standings |
| `WorldCup_Carousel_GW3.pdf` | GW2 LinkedIn carousel |

---

## Tools & Methods

Python · pandas · scipy · statsmodels · plotly · seaborn

Spearman correlation · Bonferroni correction · Poisson regression · Monte Carlo simulation · Elo ratings (eloratings.net)

---

## Data Sources

- Kaggle — international football results 1872–2026
- WhoScored — team statistics 2014 & 2018
- FIFA official records — 2022 tournament data
- eloratings.net — Elo ratings updated after every match

## Live Updates
Model re-runs after every gameweek → [View all updates](Updates)
