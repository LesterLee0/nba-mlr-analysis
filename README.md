# 🏀 NBA Game Statistics: Multiple Linear Regression Analysis

This project investigates the impact of various in-game statistics on the total points scored in NBA games using **Multiple Linear Regression (MLR)**. This is part of a course project for **Stats 101A**.

## Objective
- Develop a regression model to predict total points scored in a game
- Identify key statistical predictors (MIN, AST, REB, Win/Loss)
- Evaluate model fit and assumptions
- Interpret coefficients and run model diagnostics

## Dataset Summary

| Metric     | Min | 1st Qu. | Median | Mean | 3rd Qu. | Max |
|------------|-----|---------|--------|------|---------|-----|
| Minutes    | 240 | 240     | 240    | 241.4| 240     | 290 |
| Points     | 73  | 105     | 114    | 114.2| 123     | 157 |
| Assists    | 11  | 23      | 27     | 26.7 | 30      | 50  |
| Rebounds   | 25  | 39      | 43     | 43.5 | 48      | 74  |

## Final Regression Model

| Term        | Estimate | Std. Error | p-value | Interpretation |
|-------------|----------|------------|---------|----------------|
| Assists     | 1.204    | 0.039      | <0.001  | Strongest predictor |
| Rebounds    | -0.062   | 0.030      | 0.042   | Slight negative effect |
| Minutes     | 0.316    | 0.030      | <0.001  | Positive effect |
| WinLoss (W) | 8.854    | 0.416      | <0.001  | Winning teams score ~9 more points |

**Adjusted R² = 0.4793**  
**VIF values** all < 2 → No multicollinearity

## Diagnostics

-  Linearity: Residuals randomly scattered
-  Normality: Residuals follow Q-Q line
-  Homoscedasticity: Constant variance of residuals
-  Low leverage 

## Model Selection

Used **stepwise regression** based on AIC. The final model maintains an adjusted R² ≈ of 48%.

## Conclusion

This regression model shows that:
- Assists and Minutes are strong positive predictors
- Winning teams score significantly more
- Rebounds have a surprisingly slight adverse effect (may reflect game pace or shooting efficiency)

## Tools
- R for model fitting and plotting

---

📌 *This project demonstrates how statistical modeling and sports analytics intersect to generate actionable insights.*

---

## 📂 Project Files

- 📄 [Final Report (PDF)](Project.pdf)  
- 🧮 [NBA Game Dataset (Excel)](Dataset.xlsx)  
- 📜 [R Markdown Script](Project.Rmd)

