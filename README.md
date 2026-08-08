# AI-Based Football Scouting: A Critical Approach

## Research Context

This project is the practical/technical counterpart to a broader thesis on
AI-driven scouting in football. The central argument: as AI-based scouting
becomes more accessible, using efficiency-oriented metrics (xG, xT, VAEP) as
the primary tool for early player evaluation tends to produce behavioral
convergence rather than genuinely better talent identification. Historically,
many of Brazilian football's most valuable players emerged from environments
with little to no early measurement — an absence that left room for
non-linear creativity to develop unpruned. As computer vision and metric-driven
evaluation reach earlier stages of player development, players and coaching
staffs face pressure to optimize for the indicator itself (Goodhart's Law,
Campbell's Law) rather than for the game's actual technical ceiling — a
dynamic further reinforced by the observer effect, where the act of
measurement itself narrows the behavioral variability from which creativity
emerges. The proposed long-term solution is not to discard efficiency metrics,
but to complement them with two additional, non-hierarchical dimensions:
a Creative Decision Rating (CDR), capturing statistically uncommon decisions
that still hold footballing value, and a Behavioral Diversity Index (BDI),
measuring the richness of a player's technical-tactical repertoire over time.

## Project Phases

### Phase 1 (current) — Efficiency-based baseline
A traditional cost-benefit scouting system using market value and
performance statistics (goals, assists) for Brazilian Série A players.
This deliberately represents the type of system the thesis critiques —
built here as a technical foundation and as a baseline for future comparison,
not as a proposed solution.

### Phase 2 (planned) — Behavioral diversity approximation
Explore simplified statistical proxies for "repertoire diversity" (e.g.
dribbles attempted, progressive passes, actions in atypical field zones)
as an approximation of the Behavioral Diversity Index (BDI) concept —
without computer vision.

### Phase 3 (long-term vision) — Full multi-objective framework
Computer vision and video analysis to properly measure Creative Decision
Rating (CDR) and BDI, incorporating them alongside efficiency metrics in
a non-hierarchical scoring system.

## Current Scope (Phase 1)

A data analysis project applying the Moneyball concept to Brazilian football,
crossing player performance stats with market value to identify undervalued
players and group playing style profiles. Currently scoped to the Brazilian
Série A, 2024 season (the most recent season with consistent data available
across both sources below).

## Data Sources

- **Football Data from Transfermarkt** (Kaggle / [dcaribou/transfermarkt-datasets](https://github.com/dcaribou/transfermarkt-datasets))
  — clubs, players, market values, and match results.
- **Brasileirão Player Stats** ([eduardopalmieri, Kaggle](https://www.kaggle.com/datasets/eduardopalmieri/brasileiro-player-stats-2024))
  — individual match-level performance statistics.

## Known Limitations

- The Transfermarkt dataset does not include Copa do Brasil, Libertadores, or
  other continental competitions for Brazilian clubs.
- Its `appearances.csv` table (individual match-level stats) has no coverage
  for Brazilian competitions at all — only European leagues are included.
  Performance data is therefore sourced from a second dataset and merged by
  player name (rather than by ID), which introduces some matching risk.

## Status
🚧 In development — data exploration phase

## Next Steps

- Merge player, market value, and performance data into a unified dataset
- Build cost-benefit metrics combining performance and market value
- Apply clustering to identify player profiles
- Build an interactive dashboard
- Expand coverage to Copa do Brasil and Libertadores (Phase 1 scope)
- Explore automated data collection (scraping/API, e.g. FBref) to keep data
  current and reduce reliance on static downloads
- Explore behavioral diversity proxies (Phase 2)