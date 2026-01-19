# Melbourne Housing Price Prediction 

This repository contains a machine learning project that predicts house prices in Melbourne, Australia. It demonstrates the fundamental workflow of data science: from automated data retrieval to model training and prediction.

##  The Machine Learning Workflow
This project follows a 4-step process for building a predictive model:
1. **Define:** Choosing the model type (Decision Tree).
2. **Fit:** Training the model by capturing patterns from the data.
3. **Predict:** Generating price estimates for new data.
4. **Evaluate:** (In progress) Measuring the accuracy of those predictions.



##  Tools Used
- **Python:** The core programming language.
- **Kagglehub:** Used for automated dataset downloading and version control.
- **Pandas:** Used for data manipulation and cleaning.
- **Scikit-Learn:** Used to implement the `DecisionTreeRegressor`.
- **OS Library:** Used to handle system-agnostic file paths.

##  Data Exploration & Cleaning
Before training the model, the data was processed as follows:

### Statistical Summary
Using `describe()`, we analyzed the distribution of housing data:
- **Count:** Number of non-empty rows.
- **Mean:** The mathematical average ($\sum x / n$).
- **Std (Standard Deviation):** Measures how spread out the prices are.
- **Quartiles (25%, 50%, 75%):** Identifies entry-level vs. premium market price points.



### Handling Missing Values
To ensure model accuracy, we used `dropna(axis=0)`. This removes any row where data is missing in any column, preventing the model from learning from incomplete information.

## The Model: Decision Tree Regressor
I selected a **Decision Tree** because it mimics human decision-making by splitting data based on key features.



### Model Features ($X$)
The model uses the following features to determine price:
- Number of **Rooms**
- Number of **Bathrooms**
- **Landsize**
- **Latitude** & **Longitude** (Location-based data)

### Reproducibility
The model uses `random_state=1`. This ensures that every time the code is run, the "random" decisions made by the tree are identical, leading to consistent results for every user.

##  Results
After fitting the data, the model successfully generated predictions for Melbourne properties. 

**Sample Prediction Output:**
- Predicted Prices: `[1,035,000, 1,465,000, 1,600,000, 1,876,000, 1,636,000]`

---

##  Project Structure
- `melb_data.csv`: The raw dataset (downloaded via Kagglehub).
- `Melbourne_Housing.ipynb`: The primary notebook containing the analysis.
