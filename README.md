Gemstone Price Prediction 💎
Overview
This project predicts the price of cubic zirconia gemstones using machine learning techniques. By analyzing features like carat, cut, color, clarity, and volume, the model helps differentiate between high and low-profit gemstones, enabling better profit strategies for Gem Stones Co. Ltd. The project achieved robust performance with a Mean R² Score of 0.92 during cross-validation and a well-performing simplified regression model.

Dataset
The dataset contains data on 26,967 cubic zirconia gemstones with the following features:

Carat: Weight of the gemstone.
Cut: Quality of the cut (e.g., Ideal, Premium).
Color: Grade of the gemstone's color (D = best, J = worst).
Clarity: Absence of inclusions or blemishes (FL = flawless, I3 = level 3 inclusions).
Depth: Height of the gemstone as a percentage of its average diameter.
Table: Width of the gemstone's table as a percentage of its average diameter.
Length (mm), Width (mm), Height (mm): Physical dimensions of the gemstone.
Price: Target variable (price in USD).
Workflow
1. Data Cleaning
Handled missing values using median and mode imputation.
Capped outliers using the IQR method to retain valuable insights without skewing results.
Dropped redundant or less significant features like Unnamed: 0 and less impactful Color categories.
2. Exploratory Data Analysis (EDA)
Visualized distributions and relationships using histograms, scatter plots, and box plots.
Created a correlation heatmap to identify key relationships:
Carat and Volume were the strongest predictors of price.
3. Feature Engineering
Created a new feature: Volume (mm³) to combine length, width, and height into a single metric.
Standardized numerical features for better model performance.
Encoded categorical variables using one-hot and ordinal encoding.
4. Model Building
Final Model:
Used Linear Regression with cross-validation (10-folds).
Performance:
Cross-Validation Mean R²: 0.92
Standard Deviation: 0.00
Simpler Model:
Trained using a reduced feature set.
Training Set Performance:
RMSE: 0.30 | MAE: 0.21 | R²: 0.91
Testing Set Performance:
RMSE: 0.31 | MAE: 0.22 | R²: 0.91
Results
Feature Importance:
Dominant Features: Carat and Volume (mm³) had the highest impact on price prediction.
Clarity and cut also contributed significantly but less so compared to the top features.
Insights:
Larger gemstones with higher clarity and better cuts command premium prices.
Simplifying the model by focusing on the most relevant features still yielded strong predictive performance.

1.Clone the repository:
 
git clone https://github.com/yourusername/gemstone-price-prediction.git

