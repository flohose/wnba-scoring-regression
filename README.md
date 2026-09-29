# Connecticut Sun Scoring Model — 2025 WNBA Season

Multiple linear regression identifying which in-game stats best predict points scored by the Connecticut Sun across the 2025 WNBA season.

## Question
Which stats (field goal %, rebounds, three-point %, steals) predict Sun scoring, and does allowing them to interact improve the model?

## Data
2025 WNBA box scores, one row per team per game, filtered to Connecticut Sun games (n = 47).

## Results
A base model with four predictors explained ~47% of scoring variation (Adjusted R² = 0.4666). Adding three significant interaction terms (FG% × 3P%, Rebounds × 3P%, 3P% × Steals) raised that to ~56% (Adjusted R² = 0.5645). For a game with 45.4 FG%, 34 rebounds, 36 3P%, and 7 steals, the final model predicts the Sun will score 79.86 points (95% CI: 77.41–82.32).

## Files
- `wnba_sun_scoring_model.Rmd`: full analysis (data wrangling, models, residual checks, prediction)
- `wnba_sun_scoring_model.html`: knitted report (download and open in a browser to view)
- `WNBA_2025_box-scores.csv`: the dataset

## Tools
Written in **R** using R Markdown. Packages: `dplyr`, `ggplot2`, `car`, `olsrr`, `kableExtra`, `stargazer`.

## How to run
1. Clone this repo and keep all three files in the same folder.
2. In R, install the packages once:
```r
   install.packages(c("rmarkdown", "dplyr", "ggplot2", "car", "olsrr", "kableExtra", "stargazer"))
```
3. Open the `.Rmd` in RStudio and click **Knit**, or run:
```r
   rmarkdown::render("wnba_sun_scoring_model.Rmd")
```

---
Course project for STAT 319 (Applied Statistics), Spring 2026.
