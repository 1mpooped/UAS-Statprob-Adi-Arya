# UAS-Statprob-Adi-Arya
# Linear Regression Analysis Documentation

## 1. Data
- Dataset: AIS (Australian Institute of Sport) dataset
- Variables:
  - Dependent: Hematocrit levels
  - Independent: Hemoglobin levels
- Population: Male athletes only
- Data Processing:
  - Subset creation for male athletes
  - Column selection for hematocrit and hemoglobin
  - Outlier removal using boxplot analysis

## 2. Assumption Testing
### a) Normality
- Method: Histogram analysis
- Tools: Built-in R histogram function
- Result: Distribution appears approximately normal for both variables

### b) Linearity
- Method: Q-Q Plot analysis
- Tools: ggplot2 package
- Result: Clear linear relationship observed between variables

### c) Homoscedasticity
- Method: Breusch-Pagan test
- Tools: lmtest package
- Result: p-value = 0.6 (> 0.05), indicating homoscedastic residuals
- Interpretation: Constant variance assumption satisfied

### d) Independence
- Validated through data collection process
- Observations from different athletes are independent

## 3. Analysis
- Model: Simple Linear Regression
- Equation: Hematocrit = β₀ + β₁(Hemoglobin) + ε
- Hypothesis Testing:
  - H₀: No relationship between variables
  - H₁: Relationship exists between variables
- Results:
  - R² = 0.74 (74% variance explained)
  - Significant p-value (< 0.05)
  - Null hypothesis rejected

## 4. Visualization
- Implemented visualizations:
  - Boxplots for outlier detection
  - Histograms for normality assessment
  - Q-Q plots for linearity verification
- Tools used:
  - Base R graphics
  - ggplot2
  - lattice

## 5. Interpretation
- Model Performance:
  - Strong predictive capability (74% variance explained)
  - Statistically significant relationship confirmed
  - All regression assumptions satisfied
- Practical Implications:
  - Hemoglobin levels can reliably predict hematocrit levels
  - Model suitable for predictive purposes in male athletes
  - Clean data (outliers removed) improves model reliability
