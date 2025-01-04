# Analysis of the Effectiveness of the Police Initiative to Reduce Violent Crime Rates in Philadelphia

## Project Description

This project analyzes the effectiveness of a **smart policing initiative** implemented by the Philadelphia Police Department (PPD) to reduce violent crime rates. The initiative, funded by the Bureau of Justice Statistics, employed data-driven strategies to identify and target crime hotspots. The analysis evaluates whether the initiative led to a **statistically significant decrease** in violent crime rates across Philadelphia and within identified hotspots.

## Goals
1. Determine if violent crime rates decreased statistically significantly in Philadelphia overall.
2. Identify violent crime hotspots and assess whether the initiative led to a significant reduction in crime within these areas.
3. Compare statistical significance using various methods for determining hotspots and different statistical techniques.

## Dataset Description

- **Data Source**: Violent crime data from 2007-2022.
- **Instances**: 1,090,720 violent crime records.
- **Features**: Year, street location, and other added attributes for analysis.

## Proposed Methods

1. **Overall Crime Trends**:
   - Linear regression to evaluate the overall trend in violent crime rates.
   - Mann-Kendall test for non-parametric trend analysis.
   - Repeated Measures ANOVA to compare differences across time.

2. **Hotspot Analysis**:
   - Use z-score thresholds and clustering techniques (e.g., K-Means) to identify hotspots.
   - Compare statistical differences in crime rates within identified hotspots using Repeated Measures ANOVA and Mann-Kendall tests.

## Results Summary

### Overall Philadelphia
- **Linear Regression**: Slope = -2829.536, P-Value = 0.000337.
- **Repeated Measures ANOVA**: F-Statistic = 2.507, P-Value = 0.01417.
- **Mann-Kendall Test**: P-Value = 0.0027.

### Hotspot Analysis
- **Hotspot Streets**:
  - 13,026 streets analyzed after filtering.
  - Repeated Measures ANOVA: F-Statistic = 2.126, P-Value = 0.0377.

- **Hotspot Centers**:
  - **Set 1** (1 center): Z-value = 1.3, 6.82% of total data, P-Value = 0.0069.
  - **Set 2** (2 centers): Z-value = 1.15, P-Values = 0.0355, 0.0027.
  - **Set 3** (3 centers): Z-value = 1, P-Values = 0.0027, 0.0355, 0.0163.

## Code Details

The analysis is implemented in the `Smart_Policing_Statistical_Analysis.ipynb` notebook, which includes:
1. **Data Cleaning**: Prepares the dataset by filtering relevant records and adding features for analysis.
2. **Trend Analysis**: Implements linear regression, Mann-Kendall test, and ANOVA to evaluate crime trends.
3. **Hotspot Identification**:
   - Uses clustering (K-Means) and z-score thresholds to determine hotspots.
   - Compares the effectiveness of the policing initiative within identified areas.
4. **Visualization**: Generates charts to visualize trends, hotspots, and statistical results.

## How to Run

1. Open the Jupyter Notebook (`Smart_Policing_Statistical_Analysis.ipynb`).
2. Ensure the required libraries (e.g., NumPy, pandas, scikit-learn, statsmodels) are installed.
3. Run the notebook cells sequentially to reproduce the analysis and results.

## Dependencies

- Python 3.x
- Jupyter Notebook
- Libraries: NumPy, pandas, scikit-learn, statsmodels, matplotlib, seaborn

## References
This analysis is based on statistical methodologies for trend and hotspot analysis and leverages publicly available crime data for Philadelphia.

---

For more details, refer to the presentation and the codebase.
