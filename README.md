# Connecticut Sun Scoring Model -2025 WNBA Season

Multiple linear regression identifying which in-game stats best predict points 
scored by the Connecticut Sun across the 2025 WNBA season.

## Question
Which stats - field goal %, rebounds, three-point %, steals - predict Sun scoring, 
and does allowing them to interact improve the model?

## Data
2025 WNBA box scores, one row per team per game. Filtered to Connecticut Sun games (n = 47).

## Results
A base model with four predictors explained ~47% of scoring variation (Adjusted R² = 0.4666). 
Adding three significant interaction terms (FG%×3P%, Rebounds×3P%, 3P%×Steals) raised that 
to ~56% (Adjusted R² = 0.5645). At median stat values, the final model predicts the Sun 
score 79.86 points (95% CI: 77.41–82.32).

Course project for CSC 319 (Applied Statistics), Spring 2026.
