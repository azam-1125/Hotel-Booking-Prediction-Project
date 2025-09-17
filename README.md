# Hotel Booking Cancellation Prediction (Python)
### 🧠 Objective

Developed a machine learning model to predict hotel booking cancellations. The project aims to identify the key factors influencing cancellations, allowing hotels to optimize their operational and revenue strategies by targeting at-risk bookings with preventive measures or special offers.

### 📊 Dataset Overview

- **Source**: A local CSV file, hotel_bookings.csv.

- **Records**: 119,390 hotel booking records.

- **Features**: 32 columns covering various booking details including `lead time`, `hotel type`, `number of guests`, `market segment`, and `average daily rate (ADR)`.

> 🧼 **Preprocessing**: The dataset was extensively cleaned to handle missing values and prepare it for model training. The company column was dropped due to a high number of missing values. Missing values in agent, children, and country were imputed with their respective modes.

### ⚙️ Tools & Technologies

| Tool	| Usage |
|--------------|--------------------|
| Python (Jupyter) | Core development                      |
| Pandas, NumPy     | Data processing                       |
| Matplotlib, Seaborn | Data visualization                  |
| Scikit-learn     | Data splitting, model training, and performance metrics        |
| Excel            | Initial dataset exploration            |
---

## 📆Project Methodology & Findings
### ✅ Data Cleaning & EDA

- **Initial Analysis**: Used df.info() and df.describe() to identify missing data in key columns and understand the statistical distribution of features.

- **Missing Data Imputation**: Imputed missing values in children and agent with their modes to retain valuable data points. The country column's missing values were also filled with the most frequent country code, PRT.

- **Feature Engineering**: Converted the reservation_status_date column to a datetime format and extracted new year and month features to analyze time-based trends.

- **Exploratory Insights**:

  - The overall cancellation rate was identified as approximately 37%.

  - Visualizations revealed that City Hotel has a higher cancellation rate than Resort Hotel.

  - Cancellations show a seasonal pattern, with the highest rates occurring in January (56.7%) and December (47.7%).

  - A correlation heatmap showed key relationships between features, informing which variables would be most impactful for the model.

### ✅ Model Development & Evaluation

- **Data Transformation**: Categorical features were converted into a numerical format using LabelEncoder to prepare the data for the model.

- **Data Splitting**: The dataset was split into training (80%) and testing (20%) sets using train_test_split to ensure an unbiased evaluation of the model's performance on unseen data.

- **Model Training**: A `Decision Tree Classifier` was trained on the preprocessed training data.

- **Performance Metrics**: The model achieved a high accuracy of **92%** on the test set. A confusion matrix was also generated to provide a detailed view of the model's correct and incorrect predictions.

### 🔍 Key Findings
|Finding	|Description|
|------------|-------------|
|Overall Cancellation Rate|	The dataset has a cancellation rate of approximately 37%.|
|Hotel Type Influence	|City Hotel bookings have a higher cancellation rate than Resort Hotel bookings.|
|Seasonal Trends|	The highest cancellation rates occur in January (56.7%) and December (47.7%).|
---
### 💡 Marketing Recommendations
- 📊 **Targeted Incentives**: Offer exclusive deals or non-refundable discounts to City Hotel bookers to reduce their higher cancellation rate.

- 🎯 **Seasonal Campaigns**: Launch proactive marketing campaigns in January and December to retain customers with special offers or reminders.
### 📈 Output

`Project.ipynb`: The full project notebook with detailed code, analysis, and visualizations.

`hotel_bookings.csv`: The original dataset.

`images/`:

 - A heatmap of feature correlations : https://i.postimg.cc/WbZ9f99J/correlation-heatmap.png

 - A visual representation of the model's performance: https://i.postimg.cc/CMBJzPp6/confusion-matrix.png
