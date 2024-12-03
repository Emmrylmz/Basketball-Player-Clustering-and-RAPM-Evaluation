# Regularized Adjusted Plus-Minus (RAPM) Analysis for Basketball Data

This repository focuses on implementing Regularized Adjusted Plus-Minus (RAPM), a widely used metric in basketball analytics to evaluate individual player impact. Unlike traditional statistics that rely on box scores, RAPM leverages advanced regression techniques to isolate a player's contribution to their team's success while accounting for the context in which they play.

## What is RAPM?

Regularized Adjusted Plus-Minus (RAPM) builds upon the concept of Adjusted Plus-Minus (APM), which estimates a player’s impact by analyzing their team's net point differential (points scored minus points allowed) when they are on the court, compared to when they are off the court. However, APM is highly sensitive to noise due to limited data and multicollinearity (e.g., teammates frequently playing together).

RAPM addresses these issues by applying **regularization techniques** such as Ridge Regression (L2 regularization). This reduces overfitting and stabilizes the estimates, ensuring more reliable insights even with limited data.

### Key Features of RAPM

- **Context-Aware**: RAPM accounts for the quality of teammates and opponents, adjusting for the influence of lineups and matchups.
- **Offense and Defense**: It can separately measure offensive and defensive contributions (ORAPM and DRAPM), providing a holistic view of player impact.
- **Team-Level Synergies**: By considering combinations of players, RAPM captures the synergies and roles within a team setup.

## Why Use RAPM?

1. **Beyond Box Scores**:
   - Traditional stats (e.g., points, assists, rebounds) often fail to capture defensive impact, off-ball contributions, or intangibles. RAPM quantifies a player’s overall effect on the game.
   
2. **Team Impact**:
   - RAPM measures how a player's presence affects their team’s scoring efficiency and defensive performance, offering a more comprehensive view than raw stats.

3. **Data-Driven Insights**:
   - RAPM uses possession-level data from play-by-play logs, incorporating the dynamics of every game situation.

4. **Role Versatility**:
   - The metric adjusts for differences in playing time, roles, and the quality of competition, making it useful for comparing players across different contexts.

## Files Overview

### 1. `HOME_AWAY_FIVES_SETUP.ipynb`

- **Purpose**: Prepares the dataset by analyzing and structuring team data based on home and away games. It sets up five-player lineups for further analysis.
- **Contents**:
  - Data loading and preprocessing.
  - Identification and assignment of lineups for home and away teams.
  - Setup for downstream RAPM calculations.
- **Outputs**: A structured dataset ready for RAPM model implementation.

### 2. `RAPM_APPLICATION.ipynb`

- **Purpose**: Implements the RAPM calculation methodology using the prepared dataset.
- **Contents**:
  - Explanation of the RAPM methodology.
  - Regularized regression techniques (e.g., Ridge Regression) for computing player impact scores.
  - Evaluation of player contributions based on offensive and defensive performance.
  - Visualization and interpretation of results.
- **Outputs**: 
  - RAPM scores for players.
  - Insights into player contributions to team success.

## Prerequisites

To run these notebooks, you need the following installed:
- Python 3.7+
- Jupyter Notebook or JupyterLab
- Required Python libraries:
  - `pandas`
  - `numpy`
  - `scikit-learn`
  - `matplotlib`
  - `seaborn`

Install dependencies using the command:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn

```
## References

- [Deep Dive on Regularized Adjusted Plus-Minus: Introductory Example](https://squared2020.com/2017/09/18/deep-dive-on-regularized-adjusted-plus-minus-i-introductory-example/)  
  A detailed explanation and example of how Regularized Adjusted Plus-Minus (RAPM) works, including the mathematical foundations and practical insights.

# Feel free to contact me  emmryilmaz@gmail.com
