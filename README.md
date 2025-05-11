# ⚡ Household Energy Consumption Analysis with Python

This project analyzes household energy usage patterns based on factors like household size, air conditioning (AC) presence, and temporal data. Using Python and machine learning, we draw actionable insights and build predictive models for energy consumption.

---

## 📊 Project Overview

### Goals:

- Understand how AC usage and household size impact energy consumption
- Analyze peak hour energy usage behavior
- Build and compare predictive models to estimate energy consumption

### Key Tasks:

- Convert and clean raw data (`datetime`, `NaN`, type conversions)
- Visualize energy consumption patterns
- Correlate household features with energy usage
- Train and evaluate multiple regression models
- Save trained models for later use

### Insights:

- Households without AC use ~29% less energy overall and ~44.8% less during peak hours  
- Smaller households consume less energy consistently  
- Household size is positively correlated with both total and peak hour consumption

---

## 🤖 Machine Learning Models

Three regression models were trained to predict energy consumption:

| Model                 | R² Score |
|----------------------|----------|
| Linear Regression     | 0.838    |
| Decision Tree Regressor | 0.989 |
| Random Forest Regressor | 0.993 |

> 🏆 **Random Forest** had the best performance, closely followed by the Decision Tree.

All models were saved as `.pkl` files for reuse:

```python
with open('../Model/randomforest_model.pkl', 'wb') as f:
    pickle.dump(randomforest_model, f)
```
### 🔧 Getting Started
#### Prerequisites
- Python 3.x
- pandas
- scikit-learn
- plotly

#### Installation
```bash
git clone https://github.com/yourusername/energy-consumption-analysis.git
cd energy-consumption-analysis
```
