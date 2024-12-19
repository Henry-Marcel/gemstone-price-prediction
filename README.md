# Gemstone Price Prediction 💎

### Overview
This project predicts the price of cubic zirconia gemstones using machine learning techniques. By analyzing features like carat, cut, color, clarity, and volume, the model helps distinguish between high and low-profit gemstones. The project achieved a **Mean R² Score of 0.92** during cross-validation and demonstrated excellent performance using a simplified model.

---

## Dataset
The dataset contains the following features:
- **Carat**: Weight of the gemstone.
- **Cut**: Quality of the cut (e.g., Ideal, Premium).
- **Color**: Grade of the gemstone's color (D = best, J = worst).
- **Clarity**: Absence of inclusions or blemishes (FL = flawless, I3 = level 3 inclusions).
- **Depth**: Height of the gemstone as a percentage of its average diameter.
- **Table**: Width of the gemstone's table as a percentage of its average diameter.
- **Length (mm)**, **Width (mm)**, **Height (mm)**: Physical dimensions of the gemstone.
- **Price**: Target variable (price in USD).

---

## Workflow
### 1. **Data Preprocessing**
- Handled missing values using median and mode imputation.
- Capped outliers using the IQR method to reduce skewness while preserving insights.
- Dropped redundant columns like `Unnamed: 0` and less impactful `Color` categories.
- Created a new feature: **Volume (mm³)** to summarize gemstone dimensions.

### 2. **Exploratory Data Analysis (EDA)**
- Visualized distributions and relationships using histograms, scatter plots, and box plots.
- Identified key relationships:
  - **Carat** and **Volume (mm³)** were the strongest predictors of price.

### 3. **Feature Engineering**
- Encoded categorical features:
  - **Ordinal Encoding** for `Cut` and `Clarity`.
  - **One-Hot Encoding** for `Color`.
- Standardized numerical features for improved model performance.

### 4. **Model Building**
- **Linear Regression with Cross-Validation**:
  - **Cross-Validation R² Scores**: 
    - [0.92633347, 0.91145528, 0.92051124, 0.92573596, 0.92087431, 0.92200948, 0.9253046, 0.93111846, 0.91931777, 0.92304208]
  - **Mean R² Score**: 0.92
  - **Standard Deviation**: 0.00
- **Simpler Model Performance**:
  - **Training Set**:
    - RMSE: 0.30, MAE: 0.21, R²: 0.91
  - **Testing Set**:
    - RMSE: 0.31, MAE: 0.22, R²: 0.91

---

## Results
- **Key Insights**:
  - Larger gemstones (higher carat and volume) with better clarity and cuts command higher prices.
  - Simplifying the model by focusing on the most relevant features still yielded excellent performance.
- **Model Effectiveness**:
  - The Linear Regression model performed consistently across training and testing sets, with minimal overfitting.

---

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/gemstone-price-prediction.git
   
2. Navigate to the project directory
   ```bash
   cd gemstone-price-prediction
   
3. Install dependencies:
   ```bash
   pip install -r requirements.txt

4. Run the notebook:
   ```bash
   jupyter notebook notebooks/gemstone_price_prediction.ipynb

