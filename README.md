# Fantasy NBA Player Draft Optimizer & Analysis

An end-to-end analysis combining **Yahoo Fantasy Basketball API** and **NBA API** data to evaluate player value vs. market perception — helping fantasy managers make smarter draft, waiver, and trade decisions.

## Overview

Fantasy basketball success depends on identifying players whose real performance outpaces their perceived value. This project engineers custom scoring metrics to surface underrated players and reveal gaps between on-court production and manager sentiment.

## Key Questions Answered

- Which players are underrated relative to their ownership percentage?
- Which stats most influence fantasy ownership?
- Which players provided the best and worst draft value?
- Which NBA teams produce the strongest fantasy contributors?

## Methodology

### Data Sources
- **Yahoo Fantasy API** — ownership %, draft position, fantasy points
- **NBA API** — real on-court stats (PTS, REB, AST, STL, BLK, 3PTM)

### Feature Engineering
- **PERF_SCORE** — composite metric measuring true on-court fantasy value
- **UNDER_SCORE** — gap between PERF_SCORE and ownership %, identifying undervalued players

### Analysis
- EDA on ownership patterns and draft behavior
- Undervalued player identification
- Feature importance analysis (which stats drive ownership)
- Team-level fantasy value comparison

## Stack

- Python, Pandas, NumPy
- Yahoo Fantasy API (`yahoo_fantasy_api`, `yahoo_oauth`)
- NBA API (`nba_api`)
- Matplotlib, Seaborn

## Key Findings

- **Brook Lopez** and **Isaiah Jackson** ranked significantly higher in PERF_SCORE than ownership suggested
- **Toronto, Denver, Boston** led in team-wide fantasy value
- Ownership is heavily driven by points and assists — defensive stats are systematically undervalued

## Setup

```bash
pip install yahoo_fantasy_api yahoo_oauth nba_api pandas numpy matplotlib seaborn
```

Yahoo OAuth2 credentials required. Create `oauth2.json` with your Yahoo API keys.

## Author

Daniel (Heedong) Jang | [hdjang.com](https://hdjang.com) | CMU Heinz '26
