 📊 Annual Survey Data Analysis

This project performs data cleaning, preprocessing, and visualization on an annual survey dataset containing industry-related information such as employment, income, and other economic indicators.

📁 Dataset
File: `annual_survey.csv`  
The dataset includes the following key features:
- `year`: Survey year (2011–2024)
- `industry_code_ANZSIC`: ANZSIC industry code
- `industry_name_ANZSIC`: Industry name
- `rme_size_grp`: Size group based on Rolling Mean Employees (RME)
- `variable`: Type of measurement (e.g., income, wages, employees)
- `value`: The recorded value (e.g., salary, count)
- `unit`: Measurement unit (e.g., DOLLARS, COUNT)
The dataset also contained several unnamed columns which were removed during cleaning.

   🧼 Data Preprocessing
Steps performed:
- Dropped unnecessary unnamed columns
- Converted `value` to numeric format
- Removed rows with missing `value`
- Filled missing categorical data with the mode
- Encoded categorical variables using `LabelEncoder`
- Imputed remaining missing numerical values with the mean

 📊 Visualizations
The following visualizations were generated using `seaborn` and `matplotlib`:
1. **Histogram** – Distribution of the `value` column  
2. **Barplot** – Average value per year  
3. **Boxplot** – Value distribution across RME size groups  
4. **Correlation Heatmap** – Between numeric and encoded features
These help in understanding trends and identifying potential features for modeling.

 🤖 Machine Learning Ready
 
The code prepares the dataset for classification or regression tasks by:
- Encoding all categorical variables
- Handling missing data
- Cleaning column types
No model training is performed in the current version but the dataset is ready for it.
Models imported for future use:
- Logistic Regression
- Random Forest Classifier
- Support Vector Machine (SVC)

⚙️ How to Run

1. Clone the repository or open in Google Colab
2. Upload the `annual_survey.csv` file manually if using Colab
3. Run the script cell-by-cell
4. View the output plots and preprocessing steps
```python
# In Google Colab
from google.colab import files
uploaded = files.upload()

import pandas as pd
df = pd.read_csv("annual_survey.csv")
