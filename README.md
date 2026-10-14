# Ames Housing Price Prediction

## Project Overview
This project explores residential house price prediction using the Ames Housing dataset. It uses exploratory data analysis, feature selection, data preprocessing, feature transformation, and Linear Regression to predict house sale prices.

The project is part of my hands-on learning journey in Machine Learning, with a focus on understanding the complete regression workflow.

## Dataset
- **Dataset:** Ames Housing
- **Input file:** `train.csv`
- **Dataset dimensions:** 1,460 rows and 81 columns
- **Target variable:** `SalePrice`

The dataset contains information about residential properties, including lot size, overall quality, living area, garage characteristics, and neighborhood.

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Project Workflow

### 1. Exploratory Data Analysis
- Inspected dataset structure and statistical summaries.
- Examined missing values and numerical feature distributions.
- Explored correlations and relationships between features and sale prices.
- Created visualizations to better understand the data.

### 2. Feature Selection
Selected 13 input features based on initial exploration and their potential relevance to house prices.

### 3. Data Preprocessing
- Split the dataset into training and testing sets.
- Used median imputation for missing `LotFrontage` values.
- Applied one-hot encoding to the `Neighborhood` feature.
- Used `ColumnTransformer` to combine preprocessing steps.

### 4. Feature Engineering
Experimented with `log1p` transformations on `LotFrontage` and `LotArea` to investigate whether transforming numerical features improves model performance.

### 5. Model Training
Trained a Linear Regression model using scikit-learn and compared three feature-selection/preprocessing experiments.

### 6. Model Evaluation
Evaluated model performance using:
- R² score
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)

## Results

The best-performing experiment among the three reported runs achieved:

| Metric | Result |
|---|---:|
| Training R² | 0.8556 |
| Testing R² | 0.7172 |
| Test MAE | 22,610.57 |
| Test MSE | 2,001,798,162.10 |

The test R² indicates that the model explains approximately 71.72% of the variation in sale prices for the current test split.

The difference between training and testing performance indicates that further improvements in generalization may be possible.

## Key Learnings
- Exploring real-world tabular datasets.
- Identifying and handling missing values.
- Selecting useful numerical and categorical features.
- Applying one-hot encoding and logarithmic transformations.
- Using `SimpleImputer`, `Pipeline`, and `ColumnTransformer`.
- Training and evaluating a regression model.
- Comparing experiments using training and testing metrics.

## Future Improvements
- Evaluate the model using cross-validation.
- Investigate the training-testing performance gap.
- Compare Linear Regression with Ridge and other regression models.
- Evaluate additional features and transformations.
- Add further regression metrics and prediction visualizations.

## How to Run
1. Clone or download this repository.
2. Install the required libraries:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```

3. Ensure `train.csv` is available in the expected working directory.
4. Open `house_price_prediction.ipynb` in Jupyter Notebook.
5. Run the notebook cells in order.

## Project Status
In progress — a practical Machine Learning project focused on regression, feature engineering, and model evaluation.

## Acknowledgements
The Ames Housing dataset is widely used for learning and experimenting with regression techniques.
